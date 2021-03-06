# ImprovedThreadLocal
This is improved ThreadLocal class that does not leak class loaders when you redeploy your web application. It is completely non-blocking so you will not have thread contention while reading, setting or initializing threadLocal values.

# SafeThreadLocal
This implementation of ThreadLocal preserves non-synchronous read access to thread local values but setting the values is a blocking operation. Use this class in a very rare situation where you need a reference from thread local value to threadLocal object. If your goal is to get rid of class loader leaks during redeployment and still have completely non-blocking acces to threadLocal values then it is better to use ImprovedThreadLocal
