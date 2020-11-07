---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 78815aaa29c46e455f24ce0daac167b2806b6c20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703417"
---
# <span data-ttu-id="a553a-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a553a-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="a553a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a553a-102">SYNOPSIS</span></span>
<span data-ttu-id="a553a-103">Azure 저장소 큐에 대 한 저장 된 액세스 정책 또는 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a553a-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a553a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a553a-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="a553a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a553a-105">DESCRIPTION</span></span>
<span data-ttu-id="a553a-106">**AzureStorageQueueStoredAccessPolicy** Cmdlet은 Azure 저장소 큐에 대해 저장 된 액세스 정책 또는 정책을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a553a-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="a553a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a553a-107">EXAMPLES</span></span>

### <span data-ttu-id="a553a-108">예제 1: 큐에 저장 된 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="a553a-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="a553a-109">이 명령은 MyQueue 이라는 저장소 큐에 Policy12 라는 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a553a-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="a553a-110">예제 2: 큐에 저장 된 모든 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="a553a-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="a553a-111">이 명령은 MyQueue 이라는 큐에 저장 된 모든 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a553a-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="a553a-112">변수</span><span class="sxs-lookup"><span data-stu-id="a553a-112">PARAMETERS</span></span>

### <span data-ttu-id="a553a-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="a553a-113">-Context</span></span>
<span data-ttu-id="a553a-114">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a553a-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a553a-115">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a553a-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a553a-116">-정책</span><span class="sxs-lookup"><span data-stu-id="a553a-116">-Policy</span></span>
<span data-ttu-id="a553a-117">이 SA (공유 액세스 서명) 토큰에 대 한 사용 권한을 포함 하는 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a553a-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a553a-118">-큐</span><span class="sxs-lookup"><span data-stu-id="a553a-118">-Queue</span></span>
<span data-ttu-id="a553a-119">Azure 저장소 큐 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a553a-119">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a553a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a553a-120">CommonParameters</span></span>
<span data-ttu-id="a553a-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a553a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a553a-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a553a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a553a-123">입력</span><span class="sxs-lookup"><span data-stu-id="a553a-123">INPUTS</span></span>

### <span data-ttu-id="a553a-124">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a553a-124">IStorageContext</span></span>

<span data-ttu-id="a553a-125">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a553a-125">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="a553a-126">이름</span><span class="sxs-lookup"><span data-stu-id="a553a-126">String</span></span>

<span data-ttu-id="a553a-127">' Queue ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a553a-127">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="a553a-128">출력</span><span class="sxs-lookup"><span data-stu-id="a553a-128">OUTPUTS</span></span>

### <span data-ttu-id="a553a-129">WindowsAzure. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="a553a-129">Microsoft.WindowsAzure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="a553a-130">상속자</span><span class="sxs-lookup"><span data-stu-id="a553a-130">NOTES</span></span>

## <span data-ttu-id="a553a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a553a-131">RELATED LINKS</span></span>

[<span data-ttu-id="a553a-132">새로운 AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a553a-132">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a553a-133">제거-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a553a-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a553a-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a553a-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a553a-135">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a553a-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


