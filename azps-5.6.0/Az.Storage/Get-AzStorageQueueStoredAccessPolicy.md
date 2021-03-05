---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: fbd5adc202886ae987f7739ac24d1dadbc0d41d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981435"
---
# <span data-ttu-id="2411a-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2411a-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="2411a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2411a-102">SYNOPSIS</span></span>
<span data-ttu-id="2411a-103">Azure 저장소 큐에 대한 저장된 액세스 정책 또는 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2411a-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="2411a-104">구문</span><span class="sxs-lookup"><span data-stu-id="2411a-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2411a-105">설명</span><span class="sxs-lookup"><span data-stu-id="2411a-105">DESCRIPTION</span></span>
<span data-ttu-id="2411a-106">**Get-AzStorageQueueStoredAccessPolicy** cmdlet에는 Azure 저장소 큐에 대한 저장된 액세스 정책 또는 정책이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="2411a-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="2411a-107">예제</span><span class="sxs-lookup"><span data-stu-id="2411a-107">EXAMPLES</span></span>

### <span data-ttu-id="2411a-108">예제 1: 큐에 저장된 액세스 정책 얻기</span><span class="sxs-lookup"><span data-stu-id="2411a-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="2411a-109">이 명령은 MyQueue라는 저장소 큐에서 Policy12라는 액세스 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2411a-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="2411a-110">예제 2: 큐에 저장된 모든 액세스 정책 사용</span><span class="sxs-lookup"><span data-stu-id="2411a-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="2411a-111">이 명령은 MyQueue라는 큐에 저장된 모든 액세스 정책을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="2411a-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="2411a-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2411a-112">PARAMETERS</span></span>

### <span data-ttu-id="2411a-113">-Context</span><span class="sxs-lookup"><span data-stu-id="2411a-113">-Context</span></span>
<span data-ttu-id="2411a-114">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2411a-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="2411a-115">저장소 컨텍스트를 구하기 위해 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2411a-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2411a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2411a-116">-DefaultProfile</span></span>
<span data-ttu-id="2411a-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2411a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2411a-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="2411a-118">-Policy</span></span>
<span data-ttu-id="2411a-119">이 SAS(공유 액세스 서명) 토큰에 대한 사용 권한을 포함하는 저장된 액세스 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2411a-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2411a-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="2411a-120">-Queue</span></span>
<span data-ttu-id="2411a-121">Azure Storage 큐 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2411a-121">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2411a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2411a-122">CommonParameters</span></span>
<span data-ttu-id="2411a-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2411a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2411a-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2411a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2411a-125">입력</span><span class="sxs-lookup"><span data-stu-id="2411a-125">INPUTS</span></span>

### <span data-ttu-id="2411a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="2411a-126">System.String</span></span>

### <span data-ttu-id="2411a-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2411a-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2411a-128">출력</span><span class="sxs-lookup"><span data-stu-id="2411a-128">OUTPUTS</span></span>

### <span data-ttu-id="2411a-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="2411a-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="2411a-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2411a-130">NOTES</span></span>

## <span data-ttu-id="2411a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2411a-131">RELATED LINKS</span></span>

[<span data-ttu-id="2411a-132">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2411a-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="2411a-133">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2411a-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="2411a-134">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2411a-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="2411a-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2411a-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


