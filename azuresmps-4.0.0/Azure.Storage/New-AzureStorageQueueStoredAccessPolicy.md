---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 578eef176903576778325eb8610870040a515751
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701766"
---
# <span data-ttu-id="e0e85-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e0e85-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="e0e85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0e85-102">SYNOPSIS</span></span>
<span data-ttu-id="e0e85-103">Azure 저장소 큐에 대해 저장 된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0e85-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="e0e85-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e0e85-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="e0e85-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e0e85-105">DESCRIPTION</span></span>
<span data-ttu-id="e0e85-106">**AzureStorageQueueStoredAccessPolicy** Cmdlet은 Azure 저장소 큐에 대해 저장 된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0e85-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="e0e85-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e0e85-107">EXAMPLES</span></span>

### <span data-ttu-id="e0e85-108">예제 1: 저장소 큐에 저장 된 액세스 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="e0e85-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="e0e85-109">이 명령은 MyQueue 이라는 저장소 큐에 Policy01 라는 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0e85-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="e0e85-110">변수</span><span class="sxs-lookup"><span data-stu-id="e0e85-110">PARAMETERS</span></span>

### <span data-ttu-id="e0e85-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="e0e85-111">-Context</span></span>
<span data-ttu-id="e0e85-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0e85-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e0e85-113">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0e85-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e0e85-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e0e85-114">-ExpiryTime</span></span>
<span data-ttu-id="e0e85-115">저장 된 액세스 정책이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0e85-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="e0e85-116">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="e0e85-116">-Permission</span></span>
<span data-ttu-id="e0e85-117">이 저장소 큐에 대 한 공개 액세스 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0e85-117">Specifies the level of public access to this storage queue.</span></span>

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

### <span data-ttu-id="e0e85-118">-정책</span><span class="sxs-lookup"><span data-stu-id="e0e85-118">-Policy</span></span>
<span data-ttu-id="e0e85-119">이 SAS 토큰에 대 한 사용 권한을 포함 하는 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0e85-119">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="e0e85-120">-큐</span><span class="sxs-lookup"><span data-stu-id="e0e85-120">-Queue</span></span>
<span data-ttu-id="e0e85-121">Azure 저장소 큐 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0e85-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="e0e85-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e0e85-122">-StartTime</span></span>
<span data-ttu-id="e0e85-123">저장 된 액세스 정책이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0e85-123">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="e0e85-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0e85-124">CommonParameters</span></span>
<span data-ttu-id="e0e85-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0e85-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0e85-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0e85-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0e85-127">입력</span><span class="sxs-lookup"><span data-stu-id="e0e85-127">INPUTS</span></span>

## <span data-ttu-id="e0e85-128">출력</span><span class="sxs-lookup"><span data-stu-id="e0e85-128">OUTPUTS</span></span>

## <span data-ttu-id="e0e85-129">상속자</span><span class="sxs-lookup"><span data-stu-id="e0e85-129">NOTES</span></span>

## <span data-ttu-id="e0e85-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0e85-130">RELATED LINKS</span></span>

[<span data-ttu-id="e0e85-131">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e0e85-131">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="e0e85-132">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e0e85-132">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e0e85-133">제거-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e0e85-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="e0e85-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e0e85-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


