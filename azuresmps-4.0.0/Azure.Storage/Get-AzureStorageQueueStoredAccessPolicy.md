---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: ''
schema: 2.0.0
ms.openlocfilehash: 552b1e638034cf0cec5825b742af4984b688cec3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524020"
---
# <span data-ttu-id="02f37-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="02f37-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="02f37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02f37-102">SYNOPSIS</span></span>
<span data-ttu-id="02f37-103">Azure 저장소 큐에 대 한 저장 된 액세스 정책 또는 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="02f37-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="02f37-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02f37-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="02f37-105">설명은</span><span class="sxs-lookup"><span data-stu-id="02f37-105">DESCRIPTION</span></span>
<span data-ttu-id="02f37-106">**AzureStorageQueueStoredAccessPolicy** Cmdlet은 Azure 저장소 큐에 대해 저장 된 액세스 정책 또는 정책을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="02f37-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="02f37-107">예제의</span><span class="sxs-lookup"><span data-stu-id="02f37-107">EXAMPLES</span></span>

### <span data-ttu-id="02f37-108">예제 1: 큐에 저장 된 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="02f37-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="02f37-109">이 명령은 MyQueue 이라는 저장소 큐에 Policy12 라는 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="02f37-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="02f37-110">예제 2: 큐에 저장 된 모든 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="02f37-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="02f37-111">이 명령은 MyQueue 이라는 큐에 저장 된 모든 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="02f37-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="02f37-112">변수</span><span class="sxs-lookup"><span data-stu-id="02f37-112">PARAMETERS</span></span>

### <span data-ttu-id="02f37-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="02f37-113">-Context</span></span>
<span data-ttu-id="02f37-114">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02f37-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="02f37-115">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="02f37-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="02f37-116">-정책</span><span class="sxs-lookup"><span data-stu-id="02f37-116">-Policy</span></span>
<span data-ttu-id="02f37-117">이 SA (공유 액세스 서명) 토큰에 대 한 사용 권한을 포함 하는 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02f37-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="02f37-118">-큐</span><span class="sxs-lookup"><span data-stu-id="02f37-118">-Queue</span></span>
<span data-ttu-id="02f37-119">Azure 저장소 큐 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02f37-119">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="02f37-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02f37-120">CommonParameters</span></span>
<span data-ttu-id="02f37-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02f37-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02f37-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02f37-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02f37-123">입력</span><span class="sxs-lookup"><span data-stu-id="02f37-123">INPUTS</span></span>

## <span data-ttu-id="02f37-124">출력</span><span class="sxs-lookup"><span data-stu-id="02f37-124">OUTPUTS</span></span>

## <span data-ttu-id="02f37-125">상속자</span><span class="sxs-lookup"><span data-stu-id="02f37-125">NOTES</span></span>

## <span data-ttu-id="02f37-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02f37-126">RELATED LINKS</span></span>

[<span data-ttu-id="02f37-127">새로운 AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="02f37-127">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="02f37-128">제거-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="02f37-128">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="02f37-129">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="02f37-129">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="02f37-130">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="02f37-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


