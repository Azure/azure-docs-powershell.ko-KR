---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: c6f0c713302ef8761c85da6d54404f86ff9fb814
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876197"
---
# <span data-ttu-id="f5244-101">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f5244-101">Set-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="f5244-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5244-102">SYNOPSIS</span></span>
<span data-ttu-id="f5244-103">Azure 저장소 큐에 대해 저장 된 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5244-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="f5244-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5244-104">SYNTAX</span></span>

```
Set-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5244-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f5244-105">DESCRIPTION</span></span>
<span data-ttu-id="f5244-106">**AzStorageQueueStoredAccessPolicy** Cmdlet은 Azure 저장소 큐에 대해 저장 된 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5244-106">The **Set-AzStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="f5244-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f5244-107">EXAMPLES</span></span>

### <span data-ttu-id="f5244-108">예제 1: 모든 권한을 사용 하 여 큐에 저장 된 액세스 정책 설정</span><span class="sxs-lookup"><span data-stu-id="f5244-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="f5244-109">이 명령은 MyQueue 이라는 저장소 큐의 Policy07 라는 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5244-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="f5244-110">변수</span><span class="sxs-lookup"><span data-stu-id="f5244-110">PARAMETERS</span></span>

### <span data-ttu-id="f5244-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="f5244-111">-Context</span></span>
<span data-ttu-id="f5244-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5244-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f5244-113">저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5244-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f5244-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5244-114">-DefaultProfile</span></span>
<span data-ttu-id="f5244-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5244-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5244-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f5244-116">-ExpiryTime</span></span>
<span data-ttu-id="f5244-117">저장 된 액세스 정책이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5244-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="f5244-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f5244-118">-NoExpiryTime</span></span>
<span data-ttu-id="f5244-119">액세스 정책에 만료 날짜가 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f5244-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="f5244-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="f5244-120">-NoStartTime</span></span>
<span data-ttu-id="f5244-121">이 cmdlet이 시작 시간 $Null 설정 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f5244-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="f5244-122">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="f5244-122">-Permission</span></span>
<span data-ttu-id="f5244-123">저장 된 액세스 정책에서 저장소 큐에 액세스 하는 데 필요한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5244-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="f5244-124">이는 문자열 (예: `rwd` 읽기, 쓰기 및 삭제) 이라고 한다는 점에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5244-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="f5244-125">-정책</span><span class="sxs-lookup"><span data-stu-id="f5244-125">-Policy</span></span>
<span data-ttu-id="f5244-126">저장 된 액세스 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5244-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="f5244-127">-큐</span><span class="sxs-lookup"><span data-stu-id="f5244-127">-Queue</span></span>
<span data-ttu-id="f5244-128">Azure 저장소 큐 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5244-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="f5244-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f5244-129">-StartTime</span></span>
<span data-ttu-id="f5244-130">저장 된 액세스 정책이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5244-130">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="f5244-131">-확인</span><span class="sxs-lookup"><span data-stu-id="f5244-131">-Confirm</span></span>
<span data-ttu-id="f5244-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5244-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5244-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5244-133">-WhatIf</span></span>
<span data-ttu-id="f5244-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f5244-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5244-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f5244-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5244-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5244-136">CommonParameters</span></span>
<span data-ttu-id="f5244-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5244-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5244-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5244-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5244-139">입력</span><span class="sxs-lookup"><span data-stu-id="f5244-139">INPUTS</span></span>

### <span data-ttu-id="f5244-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f5244-140">System.String</span></span>

### <span data-ttu-id="f5244-141">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f5244-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f5244-142">출력</span><span class="sxs-lookup"><span data-stu-id="f5244-142">OUTPUTS</span></span>

### <span data-ttu-id="f5244-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f5244-143">System.String</span></span>

## <span data-ttu-id="f5244-144">상속자</span><span class="sxs-lookup"><span data-stu-id="f5244-144">NOTES</span></span>

## <span data-ttu-id="f5244-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5244-145">RELATED LINKS</span></span>

[<span data-ttu-id="f5244-146">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f5244-146">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="f5244-147">새로운 AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f5244-147">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="f5244-148">제거-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f5244-148">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)
