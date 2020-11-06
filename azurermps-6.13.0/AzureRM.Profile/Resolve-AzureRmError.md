---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/resolve-azurermerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Resolve-AzureRmError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Resolve-AzureRmError.md
ms.openlocfilehash: 35e3904badd885be18268de0b0f61b14d59f7356
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534223"
---
# <span data-ttu-id="c4440-101">Resolve-AzureRmError</span><span class="sxs-lookup"><span data-stu-id="c4440-101">Resolve-AzureRmError</span></span>

## <span data-ttu-id="c4440-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4440-102">SYNOPSIS</span></span>
<span data-ttu-id="c4440-103">Azure PowerShell 오류에 대 한 자세한 세부 정보를 포함 하 여 PowerShell 오류에 대 한 자세한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4440-103">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4440-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c4440-104">SYNTAX</span></span>

### <span data-ttu-id="c4440-105">AnyErrorParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c4440-105">AnyErrorParameterSet (Default)</span></span>
```
Resolve-AzureRmError [[-Error] <ErrorRecord[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4440-106">LastErrorParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4440-106">LastErrorParameterSet</span></span>
```
Resolve-AzureRmError [-Last] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4440-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c4440-107">DESCRIPTION</span></span>
<span data-ttu-id="c4440-108">스크립트에서 오류가 발생 한 위치, 스택 추적, 모든 내부 및 집계 예외를 비롯 하 여 현재 PowerShell 세션의 오류에 대 한 자세한 정보를 확인 하 고 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4440-108">Resolves and displays detailed information about errors in the current PowerShell session, including where the error occurred in script, stack trace, and all inner and aggregate exceptions.</span></span> <span data-ttu-id="c4440-109">Azure PowerShell 오류는 오류를 일으킨 요청 및 서버 응답에 대 한 완전 한 세부 정보를 포함 하 여 서비스 문제를 디버깅 하는 데 추가 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4440-109">For Azure PowerShell errors provides additional detail in debugging service issues, including complete detail about the request and server response that caused the error.</span></span>

## <span data-ttu-id="c4440-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c4440-110">EXAMPLES</span></span>

### <span data-ttu-id="c4440-111">예제 1: 마지막 오류 해결</span><span class="sxs-lookup"><span data-stu-id="c4440-111">Example 1: Resolve the Last Error</span></span>
```
PS C:\> Resolve-AzureRmError -Last

   HistoryId: 3


Message        : Run Connect-AzureRmAccount to login.
StackTrace     :    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.get_DefaultContext() in AzureRmCmdlet.cs:line 85
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.LogCmdletStartInvocationInfo() in AzureRmCmdlet.cs:line 269
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.BeginProcessing() inAzurePSCmdlet.cs:line 299
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.BeginProcessing() in AzureRmCmdlet.cs:line 320
                    at Microsoft.Azure.Commands.Profile.GetAzureRMSubscriptionCommand.BeginProcessing() in GetAzureRMSubscription.cs:line 49
                    at System.Management.Automation.Cmdlet.DoBeginProcessing()
                    at System.Management.Automation.CommandProcessorBase.DoBegin()
Exception      : System.Management.Automation.PSInvalidOperationException
InvocationInfo : {Get-AzureRmSubscription}
Line           : Get-AzureRmSubscription
Position       : At line:1 char:1
                 + Get-AzureRmSubscription
                 + ~~~~~~~~~~~~~~~~~~~~~~~
HistoryId      : 3
```

<span data-ttu-id="c4440-112">마지막 오류에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c4440-112">Get details of the last error.</span></span>

### <span data-ttu-id="c4440-113">예제 2: 세션의 모든 오류 해결</span><span class="sxs-lookup"><span data-stu-id="c4440-113">Example 2: Resolve all Errors in the Session</span></span>
```
PS C:\> Resolve-AzureRmError


   HistoryId: 8


RequestId      : b61309e8-09c9-4f0d-ba56-08a6b28c731d
Message        : Resource group 'contoso' could not be found.
ServerMessage  : ResourceGroupNotFound: Resource group 'contoso' could not be found.
                 (System.Collections.Generic.List`1[Microsoft.Rest.Azure.CloudError])
ServerResponse : {NotFound}
RequestMessage : {GET https://management.azure.com/subscriptions/00977cdb-163f-435f-9c32-39ec8ae61f4d/resourceGroups/co
                 ntoso/providers/Microsoft.Storage/storageAccounts/contoso?api-version=2016-12-01}
InvocationInfo : {Get-AzureRmStorageAccount}
Line           : Get-AzureRmStorageAccount -ResourceGroupName contoso -Name contoso
Position       : At line:1 char:1
                 + Get-AzureRmStorageAccount -ResourceGroupName contoso -Name contoso
                 + ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
StackTrace     :    at Microsoft.Azure.Management.Storage.StorageAccountsOperations.<GetPropertiesWithHttpMessagesAsync
                 >d__8.MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.<GetPropertiesAsync>d__7.
                 MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.GetProperties(IStorageAcc
                 ountsOperations operations, String resourceGroupName, String accountName)
                    at Microsoft.Azure.Commands.Management.Storage.GetAzureStorageAccountCommand.ExecuteCmdlet() in C:\
                 zd\azure-powershell\src\ResourceManager\Storage\Commands.Management.Storage\StorageAccount\GetAzureSto
                 rageAccount.cs:line 70
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.ProcessRecord() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 642
HistoryId      : 8


   HistoryId: 5


Message        : Run Connect-AzureRmAccount to login.
StackTrace     :    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.get_DefaultContext() in C:\zd\azur
                 e-powershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:line 85
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.LogCmdletStartInvocationInfo() in
                 C:\zd\azure-powershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:lin
                 e 269
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.BeginProcessing() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 299
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.BeginProcessing() in C:\zd\azure-p
                 owershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:line 320
                    at Microsoft.Azure.Commands.Profile.GetAzureRMSubscriptionCommand.BeginProcessing() in C:\zd\azure-
                 powershell\src\ResourceManager\Profile\Commands.Profile\Subscription\GetAzureRMSubscription.cs:line 49
                    at System.Management.Automation.Cmdlet.DoBeginProcessing()
                    at System.Management.Automation.CommandProcessorBase.DoBegin()
Exception      : System.Management.Automation.PSInvalidOperationException
InvocationInfo : {Get-AzureRmSubscription}
Line           : Get-AzureRmSubscription
Position       : At line:1 char:1
                 + Get-AzureRmSubscription
                 + ~~~~~~~~~~~~~~~~~~~~~~~
HistoryId      : 5
```

<span data-ttu-id="c4440-114">현재 세션에서 발생 한 모든 오류에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c4440-114">Get details of all errors that have occurred in the current session.</span></span>

### <span data-ttu-id="c4440-115">예제 3: 특정 오류 해결</span><span class="sxs-lookup"><span data-stu-id="c4440-115">Example 3: Resolve a Specific Error</span></span>
```
PS C:\> Resolve-AzureRmError $Error[0]


   HistoryId: 8


RequestId      : b61309e8-09c9-4f0d-ba56-08a6b28c731d
Message        : Resource group 'contoso' could not be found.
ServerMessage  : ResourceGroupNotFound: Resource group 'contoso' could not be found.
                 (System.Collections.Generic.List`1[Microsoft.Rest.Azure.CloudError])
ServerResponse : {NotFound}
RequestMessage : {GET https://management.azure.com/subscriptions/00977cdb-163f-435f-9c32-39ec8ae61f4d/resourceGroups/co
                 ntoso/providers/Microsoft.Storage/storageAccounts/contoso?api-version=2016-12-01}
InvocationInfo : {Get-AzureRmStorageAccount}
Line           : Get-AzureRmStorageAccount -ResourceGroupName contoso -Name contoso
Position       : At line:1 char:1
                 + Get-AzureRmStorageAccount -ResourceGroupName contoso -Name contoso
                 + ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
StackTrace     :    at Microsoft.Azure.Management.Storage.StorageAccountsOperations.<GetPropertiesWithHttpMessagesAsync
                 >d__8.MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.<GetPropertiesAsync>d__7.
                 MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.GetProperties(IStorageAcc
                 ountsOperations operations, String resourceGroupName, String accountName)
                    at Microsoft.Azure.Commands.Management.Storage.GetAzureStorageAccountCommand.ExecuteCmdlet() in C:\
                 zd\azure-powershell\src\ResourceManager\Storage\Commands.Management.Storage\StorageAccount\GetAzureSto
                 rageAccount.cs:line 70
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.ProcessRecord() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 642
HistoryId      : 8
```

<span data-ttu-id="c4440-116">지정 된 오류에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c4440-116">Get details of the specified error.</span></span>

## <span data-ttu-id="c4440-117">변수</span><span class="sxs-lookup"><span data-stu-id="c4440-117">PARAMETERS</span></span>

### <span data-ttu-id="c4440-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4440-118">-DefaultProfile</span></span>
<span data-ttu-id="c4440-119">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c4440-119">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4440-120">-오류</span><span class="sxs-lookup"><span data-stu-id="c4440-120">-Error</span></span>
<span data-ttu-id="c4440-121">하나 이상의 오류 레코드를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4440-121">One or more error records to resolve.</span></span>  <span data-ttu-id="c4440-122">매개 변수를 지정 하지 않으면 세션의 모든 오류가 해결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4440-122">If no parameters are specified, all errors in the session are resolved.</span></span>

```yaml
Type: System.Management.Automation.ErrorRecord[]
Parameter Sets: AnyErrorParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4440-123">-마지막</span><span class="sxs-lookup"><span data-stu-id="c4440-123">-Last</span></span>
<span data-ttu-id="c4440-124">세션에서 발생 한 마지막 오류만 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4440-124">Resolve only the last error that occurred in the session.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LastErrorParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4440-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4440-125">CommonParameters</span></span>
<span data-ttu-id="c4440-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4440-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4440-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4440-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4440-128">입력</span><span class="sxs-lookup"><span data-stu-id="c4440-128">INPUTS</span></span>

### <span data-ttu-id="c4440-129">ErrorRecord []</span><span class="sxs-lookup"><span data-stu-id="c4440-129">System.Management.Automation.ErrorRecord[]</span></span>
<span data-ttu-id="c4440-130">매개 변수: Error (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c4440-130">Parameters: Error (ByValue)</span></span>

## <span data-ttu-id="c4440-131">출력</span><span class="sxs-lookup"><span data-stu-id="c4440-131">OUTPUTS</span></span>

### <span data-ttu-id="c4440-132">AzureErrorRecord를 통해 발생 하는 파일.</span><span class="sxs-lookup"><span data-stu-id="c4440-132">Microsoft.Azure.Commands.Profile.Errors.AzureErrorRecord</span></span>

### <span data-ttu-id="c4440-133">Microsoft. Azure. 명령 프로필. AzureExceptionRecord</span><span class="sxs-lookup"><span data-stu-id="c4440-133">Microsoft.Azure.Commands.Profile.Errors.AzureExceptionRecord</span></span>

### <span data-ttu-id="c4440-134">AzureRestExceptionRecord를 통해 발생 하는 파일.</span><span class="sxs-lookup"><span data-stu-id="c4440-134">Microsoft.Azure.Commands.Profile.Errors.AzureRestExceptionRecord</span></span>

## <span data-ttu-id="c4440-135">상속자</span><span class="sxs-lookup"><span data-stu-id="c4440-135">NOTES</span></span>

## <span data-ttu-id="c4440-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4440-136">RELATED LINKS</span></span>
