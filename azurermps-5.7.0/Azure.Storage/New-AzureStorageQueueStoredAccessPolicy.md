---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: ba1759d9efb1c5e624b1ced5cddd03ee79917c4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530600"
---
# <span data-ttu-id="adc09-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="adc09-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="adc09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adc09-102">SYNOPSIS</span></span>
<span data-ttu-id="adc09-103">Azure 저장소 큐에 대해 저장 된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="adc09-103">Creates a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adc09-104">구문과</span><span class="sxs-lookup"><span data-stu-id="adc09-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="adc09-105">설명은</span><span class="sxs-lookup"><span data-stu-id="adc09-105">DESCRIPTION</span></span>
<span data-ttu-id="adc09-106">**AzureStorageQueueStoredAccessPolicy** Cmdlet은 Azure 저장소 큐에 대해 저장 된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="adc09-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="adc09-107">예제의</span><span class="sxs-lookup"><span data-stu-id="adc09-107">EXAMPLES</span></span>

### <span data-ttu-id="adc09-108">예제 1: 저장소 큐에 저장 된 액세스 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="adc09-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="adc09-109">이 명령은 MyQueue 이라는 저장소 큐에 Policy01 라는 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="adc09-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="adc09-110">변수</span><span class="sxs-lookup"><span data-stu-id="adc09-110">PARAMETERS</span></span>

### <span data-ttu-id="adc09-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="adc09-111">-Context</span></span>
<span data-ttu-id="adc09-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc09-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="adc09-113">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc09-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="adc09-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="adc09-114">-ExpiryTime</span></span>
<span data-ttu-id="adc09-115">저장 된 액세스 정책이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc09-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc09-116">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="adc09-116">-Permission</span></span>
<span data-ttu-id="adc09-117">저장 된 액세스 정책에서 저장소 큐에 액세스 하는 데 필요한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc09-117">Specifies permissions in the stored access policy to access the storage queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc09-118">-정책</span><span class="sxs-lookup"><span data-stu-id="adc09-118">-Policy</span></span>
<span data-ttu-id="adc09-119">저장 된 액세스 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc09-119">Specifies a name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc09-120">-큐</span><span class="sxs-lookup"><span data-stu-id="adc09-120">-Queue</span></span>
<span data-ttu-id="adc09-121">Azure 저장소 큐 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc09-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="adc09-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="adc09-122">-StartTime</span></span>
<span data-ttu-id="adc09-123">저장 된 액세스 정책이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc09-123">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc09-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc09-124">CommonParameters</span></span>
<span data-ttu-id="adc09-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc09-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc09-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adc09-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc09-127">입력</span><span class="sxs-lookup"><span data-stu-id="adc09-127">INPUTS</span></span>

### <span data-ttu-id="adc09-128">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="adc09-128">IStorageContext</span></span>

<span data-ttu-id="adc09-129">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc09-129">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="adc09-130">이름</span><span class="sxs-lookup"><span data-stu-id="adc09-130">String</span></span>

<span data-ttu-id="adc09-131">' Queue ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc09-131">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="adc09-132">출력</span><span class="sxs-lookup"><span data-stu-id="adc09-132">OUTPUTS</span></span>

### <span data-ttu-id="adc09-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="adc09-133">System.String</span></span>

## <span data-ttu-id="adc09-134">상속자</span><span class="sxs-lookup"><span data-stu-id="adc09-134">NOTES</span></span>

## <span data-ttu-id="adc09-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="adc09-135">RELATED LINKS</span></span>

[<span data-ttu-id="adc09-136">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="adc09-136">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="adc09-137">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="adc09-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="adc09-138">제거-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="adc09-138">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="adc09-139">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="adc09-139">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


