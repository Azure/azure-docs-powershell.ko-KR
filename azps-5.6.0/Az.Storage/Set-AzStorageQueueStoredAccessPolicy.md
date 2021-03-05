---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: e2e88cc676fddd6da7ce460fbe0d9d770756c4c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974144"
---
# <span data-ttu-id="ee28c-101">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ee28c-101">Set-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="ee28c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee28c-102">SYNOPSIS</span></span>
<span data-ttu-id="ee28c-103">Azure 저장소 큐에 대한 저장된 액세스 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee28c-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="ee28c-104">구문</span><span class="sxs-lookup"><span data-stu-id="ee28c-104">SYNTAX</span></span>

```
Set-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee28c-105">설명</span><span class="sxs-lookup"><span data-stu-id="ee28c-105">DESCRIPTION</span></span>
<span data-ttu-id="ee28c-106">**Set-AzStorageQueueStoredAccessPolicy** cmdlet은 Azure 저장소 큐에 대한 저장된 액세스 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee28c-106">The **Set-AzStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="ee28c-107">예제</span><span class="sxs-lookup"><span data-stu-id="ee28c-107">EXAMPLES</span></span>

### <span data-ttu-id="ee28c-108">예제 1: 전체 권한으로 큐에 저장된 액세스 정책 설정</span><span class="sxs-lookup"><span data-stu-id="ee28c-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="ee28c-109">이 명령은 MyQueue라는 저장소 큐에 대해 Policy07이라는 액세스 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee28c-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="ee28c-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ee28c-110">PARAMETERS</span></span>

### <span data-ttu-id="ee28c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ee28c-111">-Context</span></span>
<span data-ttu-id="ee28c-112">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee28c-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ee28c-113">저장소 컨텍스트를 구하기 위해 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee28c-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ee28c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee28c-114">-DefaultProfile</span></span>
<span data-ttu-id="ee28c-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee28c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee28c-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ee28c-116">-ExpiryTime</span></span>
<span data-ttu-id="ee28c-117">저장된 액세스 정책이 유효하지 않은 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee28c-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="ee28c-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ee28c-118">-NoExpiryTime</span></span>
<span data-ttu-id="ee28c-119">액세스 정책에 만료 날짜가 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ee28c-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="ee28c-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="ee28c-120">-NoStartTime</span></span>
<span data-ttu-id="ee28c-121">이 cmdlet은 시작 시간을 $Null.</span><span class="sxs-lookup"><span data-stu-id="ee28c-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="ee28c-122">-권한</span><span class="sxs-lookup"><span data-stu-id="ee28c-122">-Permission</span></span>
<span data-ttu-id="ee28c-123">저장소 큐에 액세스하기 위해 저장된 액세스 정책에서 권한을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee28c-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="ee28c-124">이 문자열은 읽기, 쓰기 및 삭제와 같은 `rwd` 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="ee28c-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="ee28c-125">-Policy</span><span class="sxs-lookup"><span data-stu-id="ee28c-125">-Policy</span></span>
<span data-ttu-id="ee28c-126">저장된 액세스 정책의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee28c-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="ee28c-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="ee28c-127">-Queue</span></span>
<span data-ttu-id="ee28c-128">Azure Storage 큐 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee28c-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="ee28c-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ee28c-129">-StartTime</span></span>
<span data-ttu-id="ee28c-130">저장된 액세스 정책이 유효한 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee28c-130">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="ee28c-131">-확인</span><span class="sxs-lookup"><span data-stu-id="ee28c-131">-Confirm</span></span>
<span data-ttu-id="ee28c-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee28c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee28c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee28c-133">-WhatIf</span></span>
<span data-ttu-id="ee28c-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ee28c-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee28c-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee28c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee28c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee28c-136">CommonParameters</span></span>
<span data-ttu-id="ee28c-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ee28c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee28c-138">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ee28c-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee28c-139">입력</span><span class="sxs-lookup"><span data-stu-id="ee28c-139">INPUTS</span></span>

### <span data-ttu-id="ee28c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ee28c-140">System.String</span></span>

### <span data-ttu-id="ee28c-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ee28c-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ee28c-142">출력</span><span class="sxs-lookup"><span data-stu-id="ee28c-142">OUTPUTS</span></span>

### <span data-ttu-id="ee28c-143">System.String</span><span class="sxs-lookup"><span data-stu-id="ee28c-143">System.String</span></span>

## <span data-ttu-id="ee28c-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ee28c-144">NOTES</span></span>

## <span data-ttu-id="ee28c-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee28c-145">RELATED LINKS</span></span>

[<span data-ttu-id="ee28c-146">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ee28c-146">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ee28c-147">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ee28c-147">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ee28c-148">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ee28c-148">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)
