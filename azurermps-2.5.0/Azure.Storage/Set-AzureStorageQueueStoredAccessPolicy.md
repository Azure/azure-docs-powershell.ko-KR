---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 4e1b58e2ca2586ada574b55a03287d1cc5915b6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883209"
---
# <span data-ttu-id="a6d43-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a6d43-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="a6d43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6d43-102">SYNOPSIS</span></span>
<span data-ttu-id="a6d43-103">Azure 저장소 큐에 대해 저장 된 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6d43-103">Sets a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6d43-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a6d43-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6d43-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a6d43-105">DESCRIPTION</span></span>
<span data-ttu-id="a6d43-106">**AzureStorageQueueStoredAccessPolicy** Cmdlet은 Azure 저장소 큐에 대해 저장 된 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6d43-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="a6d43-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a6d43-107">EXAMPLES</span></span>

### <span data-ttu-id="a6d43-108">예제 1: 모든 권한을 사용 하 여 큐에 저장 된 액세스 정책 설정</span><span class="sxs-lookup"><span data-stu-id="a6d43-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="a6d43-109">이 명령은 MyQueue 이라는 저장소 큐의 Policy07 라는 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6d43-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="a6d43-110">변수</span><span class="sxs-lookup"><span data-stu-id="a6d43-110">PARAMETERS</span></span>

### <span data-ttu-id="a6d43-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="a6d43-111">-Context</span></span>
<span data-ttu-id="a6d43-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6d43-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a6d43-113">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6d43-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a6d43-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6d43-114">-DefaultProfile</span></span>
<span data-ttu-id="a6d43-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6d43-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6d43-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a6d43-116">-ExpiryTime</span></span>
<span data-ttu-id="a6d43-117">저장 된 액세스 정책이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6d43-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d43-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a6d43-118">-NoExpiryTime</span></span>
<span data-ttu-id="a6d43-119">액세스 정책에 만료 날짜가 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a6d43-119">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d43-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="a6d43-120">-NoStartTime</span></span>
<span data-ttu-id="a6d43-121">이 cmdlet이 시작 시간 $Null 설정 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a6d43-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d43-122">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="a6d43-122">-Permission</span></span>
<span data-ttu-id="a6d43-123">저장 된 액세스 정책에서 저장소 큐에 액세스 하는 데 필요한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6d43-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="a6d43-124">이는 문자열 (예: `rwd` 읽기, 쓰기 및 삭제) 이라고 한다는 점에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6d43-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d43-125">-정책</span><span class="sxs-lookup"><span data-stu-id="a6d43-125">-Policy</span></span>
<span data-ttu-id="a6d43-126">저장 된 액세스 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6d43-126">Specifies the name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d43-127">-큐</span><span class="sxs-lookup"><span data-stu-id="a6d43-127">-Queue</span></span>
<span data-ttu-id="a6d43-128">Azure 저장소 큐 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6d43-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="a6d43-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a6d43-129">-StartTime</span></span>
<span data-ttu-id="a6d43-130">저장 된 액세스 정책이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6d43-130">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d43-131">-확인</span><span class="sxs-lookup"><span data-stu-id="a6d43-131">-Confirm</span></span>
<span data-ttu-id="a6d43-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6d43-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d43-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6d43-133">-WhatIf</span></span>
<span data-ttu-id="a6d43-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a6d43-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6d43-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6d43-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d43-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6d43-136">CommonParameters</span></span>
<span data-ttu-id="a6d43-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6d43-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6d43-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6d43-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6d43-139">입력</span><span class="sxs-lookup"><span data-stu-id="a6d43-139">INPUTS</span></span>

### <span data-ttu-id="a6d43-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a6d43-140">System.String</span></span>

### <span data-ttu-id="a6d43-141">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a6d43-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a6d43-142">출력</span><span class="sxs-lookup"><span data-stu-id="a6d43-142">OUTPUTS</span></span>

### <span data-ttu-id="a6d43-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a6d43-143">System.String</span></span>

## <span data-ttu-id="a6d43-144">상속자</span><span class="sxs-lookup"><span data-stu-id="a6d43-144">NOTES</span></span>

## <span data-ttu-id="a6d43-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6d43-145">RELATED LINKS</span></span>

[<span data-ttu-id="a6d43-146">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a6d43-146">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a6d43-147">새로운 AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a6d43-147">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a6d43-148">제거-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a6d43-148">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
