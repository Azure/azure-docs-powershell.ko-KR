---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: c8d41300250e41548cf949248b02c819b7da497f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217158"
---
# <span data-ttu-id="376ae-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="376ae-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="376ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="376ae-102">SYNOPSIS</span></span>
<span data-ttu-id="376ae-103">개체 복제 정책 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="376ae-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="376ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="376ae-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="376ae-105">설명은</span><span class="sxs-lookup"><span data-stu-id="376ae-105">DESCRIPTION</span></span>
<span data-ttu-id="376ae-106">**AzStorageObjectReplicationPolicy** cmdlet은 Set-AzStorageObjectReplicationPolicy cmdlet에 사용 되는 개체 복제 정책 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="376ae-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="376ae-107">예제의</span><span class="sxs-lookup"><span data-stu-id="376ae-107">EXAMPLES</span></span>

### <span data-ttu-id="376ae-108">예제 1: 원본 및 대상 계정만 사용 하 여 개체 복제 정책 규칙을 만들고 해당 속성 표시</span><span class="sxs-lookup"><span data-stu-id="376ae-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="376ae-109">이 명령은 원본 및 대상 계정만 사용 하 여 개체 복제 정책 규칙을 만들고 해당 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="376ae-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="376ae-110">예제 2: 모든 속성과 함께 개체 복제 정책 규칙 만들기 및 해당 속성 표시</span><span class="sxs-lookup"><span data-stu-id="376ae-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="376ae-111">이 명령은 모든 속성이 있는 개체 복제 정책 규칙을 사용 하 여 해당 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="376ae-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="376ae-112">변수</span><span class="sxs-lookup"><span data-stu-id="376ae-112">PARAMETERS</span></span>

### <span data-ttu-id="376ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="376ae-113">-DefaultProfile</span></span>
<span data-ttu-id="376ae-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="376ae-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="376ae-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="376ae-115">-DestinationContainer</span></span>
<span data-ttu-id="376ae-116">복제할 대상 컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="376ae-116">The Destination Container name to replicate to.</span></span>

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

### <span data-ttu-id="376ae-117">-MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="376ae-117">-MinCreationTime</span></span>
<span data-ttu-id="376ae-118">시간이 지난 후 만들어진 blob는 대상에 복제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="376ae-118">Blobs created after the time will be replicated to the destination..</span></span>

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

### <span data-ttu-id="376ae-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="376ae-119">-PrefixMatch</span></span>
<span data-ttu-id="376ae-120">이름이 지정 된 접두사로 시작 하는 blob만 복제 하도록 결과를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="376ae-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

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

### <span data-ttu-id="376ae-121">-RuleId</span><span class="sxs-lookup"><span data-stu-id="376ae-121">-RuleId</span></span>
<span data-ttu-id="376ae-122">개체 복제 규칙 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="376ae-122">Object Replication Rule Id.</span></span>

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

### <span data-ttu-id="376ae-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="376ae-123">-SourceContainer</span></span>
<span data-ttu-id="376ae-124">복제할 원본 컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="376ae-124">The Source Container name to replicate from.</span></span>

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

### <span data-ttu-id="376ae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="376ae-125">CommonParameters</span></span>
<span data-ttu-id="376ae-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="376ae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="376ae-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="376ae-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="376ae-128">입력</span><span class="sxs-lookup"><span data-stu-id="376ae-128">INPUTS</span></span>

### <span data-ttu-id="376ae-129">않아야</span><span class="sxs-lookup"><span data-stu-id="376ae-129">None</span></span>

## <span data-ttu-id="376ae-130">출력</span><span class="sxs-lookup"><span data-stu-id="376ae-130">OUTPUTS</span></span>

### <span data-ttu-id="376ae-131">PSObjectReplicationPolicyRule를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="376ae-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="376ae-132">상속자</span><span class="sxs-lookup"><span data-stu-id="376ae-132">NOTES</span></span>

## <span data-ttu-id="376ae-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="376ae-133">RELATED LINKS</span></span>
