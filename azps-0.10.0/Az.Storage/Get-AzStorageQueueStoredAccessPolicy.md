---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 9c61542aeb79cdcaa90d4ac32be4be38649e4abd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876296"
---
# <span data-ttu-id="d259b-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d259b-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="d259b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d259b-102">SYNOPSIS</span></span>
<span data-ttu-id="d259b-103">Azure 저장소 큐에 대 한 저장 된 액세스 정책 또는 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d259b-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="d259b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d259b-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d259b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d259b-105">DESCRIPTION</span></span>
<span data-ttu-id="d259b-106">**AzStorageQueueStoredAccessPolicy** Cmdlet은 Azure 저장소 큐에 대해 저장 된 액세스 정책 또는 정책을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="d259b-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="d259b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d259b-107">EXAMPLES</span></span>

### <span data-ttu-id="d259b-108">예제 1: 큐에 저장 된 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="d259b-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="d259b-109">이 명령은 MyQueue 이라는 저장소 큐에 Policy12 라는 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d259b-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="d259b-110">예제 2: 큐에 저장 된 모든 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="d259b-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="d259b-111">이 명령은 MyQueue 이라는 큐에 저장 된 모든 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d259b-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="d259b-112">변수</span><span class="sxs-lookup"><span data-stu-id="d259b-112">PARAMETERS</span></span>

### <span data-ttu-id="d259b-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="d259b-113">-Context</span></span>
<span data-ttu-id="d259b-114">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d259b-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="d259b-115">저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d259b-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d259b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d259b-116">-DefaultProfile</span></span>
<span data-ttu-id="d259b-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d259b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d259b-118">-정책</span><span class="sxs-lookup"><span data-stu-id="d259b-118">-Policy</span></span>
<span data-ttu-id="d259b-119">이 SA (공유 액세스 서명) 토큰에 대 한 사용 권한을 포함 하는 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d259b-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="d259b-120">-큐</span><span class="sxs-lookup"><span data-stu-id="d259b-120">-Queue</span></span>
<span data-ttu-id="d259b-121">Azure 저장소 큐 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d259b-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="d259b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d259b-122">CommonParameters</span></span>
<span data-ttu-id="d259b-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d259b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d259b-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d259b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d259b-125">입력</span><span class="sxs-lookup"><span data-stu-id="d259b-125">INPUTS</span></span>

### <span data-ttu-id="d259b-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d259b-126">System.String</span></span>

### <span data-ttu-id="d259b-127">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d259b-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d259b-128">출력</span><span class="sxs-lookup"><span data-stu-id="d259b-128">OUTPUTS</span></span>

### <span data-ttu-id="d259b-129">SharedAccessQueuePolicy/. \ 저장소. m a.</span><span class="sxs-lookup"><span data-stu-id="d259b-129">Microsoft.WindowsAz.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="d259b-130">상속자</span><span class="sxs-lookup"><span data-stu-id="d259b-130">NOTES</span></span>

## <span data-ttu-id="d259b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d259b-131">RELATED LINKS</span></span>

[<span data-ttu-id="d259b-132">새로운 AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d259b-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="d259b-133">제거-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d259b-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="d259b-134">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d259b-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="d259b-135">새로운 AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d259b-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


