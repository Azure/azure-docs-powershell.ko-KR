---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 9a3a19b2e0773d1513ce57dc5fe7ca7502bb325d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711851"
---
# <span data-ttu-id="1ddc1-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1ddc1-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="1ddc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ddc1-102">SYNOPSIS</span></span>
<span data-ttu-id="1ddc1-103">Azure 저장소 큐에 대해 저장 된 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ddc1-103">Sets a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ddc1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1ddc1-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ddc1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1ddc1-105">DESCRIPTION</span></span>
<span data-ttu-id="1ddc1-106">**AzureStorageQueueStoredAccessPolicy** Cmdlet은 Azure 저장소 큐에 대해 저장 된 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ddc1-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="1ddc1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1ddc1-107">EXAMPLES</span></span>

### <span data-ttu-id="1ddc1-108">예제 1: 모든 권한을 사용 하 여 큐에 저장 된 액세스 정책 설정</span><span class="sxs-lookup"><span data-stu-id="1ddc1-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="1ddc1-109">이 명령은 MyQueue 이라는 저장소 큐의 Policy07 라는 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ddc1-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="1ddc1-110">변수</span><span class="sxs-lookup"><span data-stu-id="1ddc1-110">PARAMETERS</span></span>

### <span data-ttu-id="1ddc1-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="1ddc1-111">-Context</span></span>
<span data-ttu-id="1ddc1-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ddc1-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1ddc1-113">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ddc1-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1ddc1-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="1ddc1-114">-ExpiryTime</span></span>
<span data-ttu-id="1ddc1-115">저장 된 액세스 정책이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ddc1-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="1ddc1-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="1ddc1-116">-NoExpiryTime</span></span>
<span data-ttu-id="1ddc1-117">액세스 정책에 만료 날짜가 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1ddc1-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="1ddc1-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="1ddc1-118">-NoStartTime</span></span>
<span data-ttu-id="1ddc1-119">이 cmdlet이 시작 시간 $Null 설정 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1ddc1-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="1ddc1-120">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="1ddc1-120">-Permission</span></span>
<span data-ttu-id="1ddc1-121">저장 된 액세스 정책에서 저장소 큐에 액세스 하는 데 필요한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ddc1-121">Specifies permissions in the stored access policy to access the storage queue.</span></span>

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

### <span data-ttu-id="1ddc1-122">-정책</span><span class="sxs-lookup"><span data-stu-id="1ddc1-122">-Policy</span></span>
<span data-ttu-id="1ddc1-123">저장 된 액세스 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ddc1-123">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="1ddc1-124">-큐</span><span class="sxs-lookup"><span data-stu-id="1ddc1-124">-Queue</span></span>
<span data-ttu-id="1ddc1-125">Azure 저장소 큐 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ddc1-125">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="1ddc1-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1ddc1-126">-StartTime</span></span>
<span data-ttu-id="1ddc1-127">저장 된 액세스 정책이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ddc1-127">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="1ddc1-128">-확인</span><span class="sxs-lookup"><span data-stu-id="1ddc1-128">-Confirm</span></span>
<span data-ttu-id="1ddc1-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ddc1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ddc1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ddc1-130">-WhatIf</span></span>
<span data-ttu-id="1ddc1-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1ddc1-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ddc1-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ddc1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ddc1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ddc1-133">CommonParameters</span></span>
<span data-ttu-id="1ddc1-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ddc1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ddc1-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ddc1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ddc1-136">입력</span><span class="sxs-lookup"><span data-stu-id="1ddc1-136">INPUTS</span></span>

### <span data-ttu-id="1ddc1-137">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1ddc1-137">IStorageContext</span></span>

<span data-ttu-id="1ddc1-138">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ddc1-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="1ddc1-139">이름</span><span class="sxs-lookup"><span data-stu-id="1ddc1-139">String</span></span>

<span data-ttu-id="1ddc1-140">' Queue ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ddc1-140">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="1ddc1-141">출력</span><span class="sxs-lookup"><span data-stu-id="1ddc1-141">OUTPUTS</span></span>

### <span data-ttu-id="1ddc1-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1ddc1-142">System.String</span></span>

## <span data-ttu-id="1ddc1-143">상속자</span><span class="sxs-lookup"><span data-stu-id="1ddc1-143">NOTES</span></span>

## <span data-ttu-id="1ddc1-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ddc1-144">RELATED LINKS</span></span>

[<span data-ttu-id="1ddc1-145">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1ddc1-145">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="1ddc1-146">새로운 AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1ddc1-146">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="1ddc1-147">제거-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1ddc1-147">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
