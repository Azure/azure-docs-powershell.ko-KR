---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: ''
schema: 2.0.0
ms.openlocfilehash: b273dbec3fda421574c8866a10eda0a8098513ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524131"
---
# <span data-ttu-id="79d9a-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="79d9a-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="79d9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="79d9a-103">Azure 저장소 큐에 대해 저장 된 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d9a-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="79d9a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="79d9a-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79d9a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="79d9a-105">DESCRIPTION</span></span>
<span data-ttu-id="79d9a-106">**AzureStorageQueueStoredAccessPolicy** Cmdlet은 Azure 저장소 큐에 대해 저장 된 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d9a-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="79d9a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="79d9a-107">EXAMPLES</span></span>

### <span data-ttu-id="79d9a-108">예제 1: 큐에 저장 된 액세스 정책 설정</span><span class="sxs-lookup"><span data-stu-id="79d9a-108">Example 1: Set a stored access policy in the queue</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07"
```

<span data-ttu-id="79d9a-109">이 명령은 MyQueue 이라는 저장소 큐의 Policy07 라는 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d9a-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="79d9a-110">변수</span><span class="sxs-lookup"><span data-stu-id="79d9a-110">PARAMETERS</span></span>

### <span data-ttu-id="79d9a-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="79d9a-111">-Context</span></span>
<span data-ttu-id="79d9a-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d9a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="79d9a-113">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d9a-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="79d9a-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="79d9a-114">-ExpiryTime</span></span>
<span data-ttu-id="79d9a-115">저장 된 액세스 정책이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d9a-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="79d9a-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="79d9a-116">-NoExpiryTime</span></span>
<span data-ttu-id="79d9a-117">액세스 정책에 만료 날짜가 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="79d9a-117">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79d9a-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="79d9a-118">-NoStartTime</span></span>
<span data-ttu-id="79d9a-119">이 cmdlet이 시작 시간 $Null 설정 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="79d9a-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79d9a-120">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="79d9a-120">-Permission</span></span>
<span data-ttu-id="79d9a-121">이 저장소 큐에 대 한 공개 액세스 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d9a-121">Specifies the level of public access to this storage queue.</span></span>

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

### <span data-ttu-id="79d9a-122">-정책</span><span class="sxs-lookup"><span data-stu-id="79d9a-122">-Policy</span></span>
<span data-ttu-id="79d9a-123">이 SAS 토큰에 대 한 사용 권한을 포함 하는 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d9a-123">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="79d9a-124">-큐</span><span class="sxs-lookup"><span data-stu-id="79d9a-124">-Queue</span></span>
<span data-ttu-id="79d9a-125">Azure 저장소 큐 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d9a-125">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="79d9a-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="79d9a-126">-StartTime</span></span>
<span data-ttu-id="79d9a-127">저장 된 액세스 정책이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d9a-127">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="79d9a-128">-확인</span><span class="sxs-lookup"><span data-stu-id="79d9a-128">-Confirm</span></span>
<span data-ttu-id="79d9a-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d9a-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79d9a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79d9a-130">-WhatIf</span></span>
<span data-ttu-id="79d9a-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="79d9a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79d9a-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79d9a-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79d9a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79d9a-133">CommonParameters</span></span>
<span data-ttu-id="79d9a-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d9a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79d9a-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79d9a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79d9a-136">입력</span><span class="sxs-lookup"><span data-stu-id="79d9a-136">INPUTS</span></span>

## <span data-ttu-id="79d9a-137">출력</span><span class="sxs-lookup"><span data-stu-id="79d9a-137">OUTPUTS</span></span>

## <span data-ttu-id="79d9a-138">상속자</span><span class="sxs-lookup"><span data-stu-id="79d9a-138">NOTES</span></span>

## <span data-ttu-id="79d9a-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79d9a-139">RELATED LINKS</span></span>

[<span data-ttu-id="79d9a-140">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="79d9a-140">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="79d9a-141">새로운 AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="79d9a-141">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="79d9a-142">제거-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="79d9a-142">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
