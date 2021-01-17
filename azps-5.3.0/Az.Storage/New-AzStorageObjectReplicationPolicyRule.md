---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: c8d41300250e41548cf949248b02c819b7da497f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491332"
---
# <span data-ttu-id="faaa0-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="faaa0-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="faaa0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faaa0-102">SYNOPSIS</span></span>
<span data-ttu-id="faaa0-103">개체 복제 정책 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="faaa0-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="faaa0-104">구문</span><span class="sxs-lookup"><span data-stu-id="faaa0-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faaa0-105">설명</span><span class="sxs-lookup"><span data-stu-id="faaa0-105">DESCRIPTION</span></span>
<span data-ttu-id="faaa0-106">**Get-AzStorageObjectReplicationPolicy** cmdlet은 개체 복제 정책 규칙을 만듭니다. 이 규칙은 Set-AzStorageObjectReplicationPolicy cmdlet에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="faaa0-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="faaa0-107">예제</span><span class="sxs-lookup"><span data-stu-id="faaa0-107">EXAMPLES</span></span>

### <span data-ttu-id="faaa0-108">예제 1: 원본 및 대상 계정만 사용하여 개체 복제 정책 규칙 만들기 및 해당 속성 표시</span><span class="sxs-lookup"><span data-stu-id="faaa0-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="faaa0-109">이 명령은 원본 및 대상 계정만 사용하여 개체 복제 정책 규칙을 만들고 해당 속성을 보여 주며,</span><span class="sxs-lookup"><span data-stu-id="faaa0-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="faaa0-110">예제 2: 모든 속성이 있는 개체 복제 정책 규칙 만들기 및 해당 속성 표시</span><span class="sxs-lookup"><span data-stu-id="faaa0-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="faaa0-111">이 명령은 모든 속성이 있는 개체 복제 정책 규칙을 표시하고 해당 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="faaa0-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="faaa0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="faaa0-112">PARAMETERS</span></span>

### <span data-ttu-id="faaa0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faaa0-113">-DefaultProfile</span></span>
<span data-ttu-id="faaa0-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="faaa0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faaa0-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="faaa0-115">-DestinationContainer</span></span>
<span data-ttu-id="faaa0-116">복제할 대상 컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="faaa0-116">The Destination Container name to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faaa0-117">-MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="faaa0-117">-MinCreationTime</span></span>
<span data-ttu-id="faaa0-118">시간 후에 만든 Blob은 대상에 복제됩니다.</span><span class="sxs-lookup"><span data-stu-id="faaa0-118">Blobs created after the time will be replicated to the destination..</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faaa0-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="faaa0-119">-PrefixMatch</span></span>
<span data-ttu-id="faaa0-120">결과를 필터하여 이름이 지정된 사전으로 시작하는 Blob만 복제합니다.</span><span class="sxs-lookup"><span data-stu-id="faaa0-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faaa0-121">-RuleId</span><span class="sxs-lookup"><span data-stu-id="faaa0-121">-RuleId</span></span>
<span data-ttu-id="faaa0-122">개체 복제 규칙 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="faaa0-122">Object Replication Rule Id.</span></span>

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

### <span data-ttu-id="faaa0-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="faaa0-123">-SourceContainer</span></span>
<span data-ttu-id="faaa0-124">복제할 원본 컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="faaa0-124">The Source Container name to replicate from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faaa0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faaa0-125">CommonParameters</span></span>
<span data-ttu-id="faaa0-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="faaa0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faaa0-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="faaa0-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faaa0-128">입력</span><span class="sxs-lookup"><span data-stu-id="faaa0-128">INPUTS</span></span>

### <span data-ttu-id="faaa0-129">없음</span><span class="sxs-lookup"><span data-stu-id="faaa0-129">None</span></span>

## <span data-ttu-id="faaa0-130">출력</span><span class="sxs-lookup"><span data-stu-id="faaa0-130">OUTPUTS</span></span>

### <span data-ttu-id="faaa0-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="faaa0-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="faaa0-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="faaa0-132">NOTES</span></span>

## <span data-ttu-id="faaa0-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="faaa0-133">RELATED LINKS</span></span>
