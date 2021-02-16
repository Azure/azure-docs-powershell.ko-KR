---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: e59ce4f5e3b0f1b07744e0754cf0e1cae3de7da6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192076"
---
# <span data-ttu-id="9c972-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="9c972-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="9c972-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c972-102">SYNOPSIS</span></span>
<span data-ttu-id="9c972-103">복제 상태 확인</span><span class="sxs-lookup"><span data-stu-id="9c972-103">Get the status of the replication</span></span>

## <span data-ttu-id="9c972-104">구문</span><span class="sxs-lookup"><span data-stu-id="9c972-104">SYNTAX</span></span>

### <span data-ttu-id="9c972-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9c972-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c972-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c972-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c972-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c972-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c972-108">설명</span><span class="sxs-lookup"><span data-stu-id="9c972-108">DESCRIPTION</span></span>
<span data-ttu-id="9c972-109">복제 상태 확인</span><span class="sxs-lookup"><span data-stu-id="9c972-109">Get the status of the replication</span></span>

## <span data-ttu-id="9c972-110">예제</span><span class="sxs-lookup"><span data-stu-id="9c972-110">EXAMPLES</span></span>

### <span data-ttu-id="9c972-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9c972-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="9c972-112">이 명령은 MyVol에서 복제의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9c972-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="9c972-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c972-113">PARAMETERS</span></span>

### <span data-ttu-id="9c972-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9c972-114">-AccountName</span></span>
<span data-ttu-id="9c972-115">복제 대상 볼륨의 ANF 계정 이름</span><span class="sxs-lookup"><span data-stu-id="9c972-115">The name of the ANF account of the replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c972-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c972-116">-DefaultProfile</span></span>
<span data-ttu-id="9c972-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9c972-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c972-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c972-118">-InputObject</span></span>
<span data-ttu-id="9c972-119">복제 상태를 얻을 ANF 복제 대상 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="9c972-119">The ANF replication destination volume object to get replication status</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c972-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9c972-120">-Name</span></span>
<span data-ttu-id="9c972-121">ANF 복제 대상 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="9c972-121">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c972-122">-PoolName</span><span class="sxs-lookup"><span data-stu-id="9c972-122">-PoolName</span></span>
<span data-ttu-id="9c972-123">복제 대상 볼륨의 ANF 풀 이름</span><span class="sxs-lookup"><span data-stu-id="9c972-123">The name of the ANF pool of the replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c972-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c972-124">-ResourceGroupName</span></span>
<span data-ttu-id="9c972-125">ANF 복제 대상 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="9c972-125">The resource group of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c972-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c972-126">-ResourceId</span></span>
<span data-ttu-id="9c972-127">ANF 복제 대상 볼륨의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="9c972-127">The resource id of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c972-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c972-128">CommonParameters</span></span>
<span data-ttu-id="9c972-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9c972-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c972-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9c972-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c972-131">입력</span><span class="sxs-lookup"><span data-stu-id="9c972-131">INPUTS</span></span>

### <span data-ttu-id="9c972-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9c972-132">System.String</span></span>

### <span data-ttu-id="9c972-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="9c972-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="9c972-134">출력</span><span class="sxs-lookup"><span data-stu-id="9c972-134">OUTPUTS</span></span>

### <span data-ttu-id="9c972-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="9c972-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="9c972-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9c972-136">NOTES</span></span>

## <span data-ttu-id="9c972-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c972-137">RELATED LINKS</span></span>
