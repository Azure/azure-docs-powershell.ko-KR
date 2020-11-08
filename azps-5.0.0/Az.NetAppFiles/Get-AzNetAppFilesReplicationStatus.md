---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: a2345dfe37fd43532739cdfd8000b47fb1e20906
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217610"
---
# <span data-ttu-id="ebe93-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="ebe93-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="ebe93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebe93-102">SYNOPSIS</span></span>
<span data-ttu-id="ebe93-103">복제 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="ebe93-103">Get the status of the replication</span></span>

## <span data-ttu-id="ebe93-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ebe93-104">SYNTAX</span></span>

### <span data-ttu-id="ebe93-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ebe93-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebe93-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebe93-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ebe93-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebe93-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebe93-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ebe93-108">DESCRIPTION</span></span>
<span data-ttu-id="ebe93-109">복제 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="ebe93-109">Get the status of the replication</span></span>

## <span data-ttu-id="ebe93-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ebe93-110">EXAMPLES</span></span>

### <span data-ttu-id="ebe93-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ebe93-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="ebe93-112">이 명령은 MyVol에 대 한 복제 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ebe93-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="ebe93-113">변수</span><span class="sxs-lookup"><span data-stu-id="ebe93-113">PARAMETERS</span></span>

### <span data-ttu-id="ebe93-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ebe93-114">-AccountName</span></span>
<span data-ttu-id="ebe93-115">복제 대상 볼륨의 ANF 계정 이름</span><span class="sxs-lookup"><span data-stu-id="ebe93-115">The name of the ANF account of the replication destination volume</span></span>

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

### <span data-ttu-id="ebe93-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebe93-116">-DefaultProfile</span></span>
<span data-ttu-id="ebe93-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ebe93-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebe93-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebe93-118">-InputObject</span></span>
<span data-ttu-id="ebe93-119">복제 상태를 가져오는 ANF 복제 대상 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="ebe93-119">The ANF replication destination volume object to get replication status</span></span>

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

### <span data-ttu-id="ebe93-120">-이름</span><span class="sxs-lookup"><span data-stu-id="ebe93-120">-Name</span></span>
<span data-ttu-id="ebe93-121">ANF 복제 대상 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ebe93-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ebe93-122">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ebe93-122">-PoolName</span></span>
<span data-ttu-id="ebe93-123">복제 대상 볼륨의 ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ebe93-123">The name of the ANF pool of the replication destination volume</span></span>

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

### <span data-ttu-id="ebe93-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebe93-124">-ResourceGroupName</span></span>
<span data-ttu-id="ebe93-125">ANF 복제 대상 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="ebe93-125">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ebe93-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebe93-126">-ResourceId</span></span>
<span data-ttu-id="ebe93-127">ANF 복제 대상 볼륨의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="ebe93-127">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ebe93-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebe93-128">CommonParameters</span></span>
<span data-ttu-id="ebe93-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebe93-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebe93-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ebe93-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebe93-131">입력</span><span class="sxs-lookup"><span data-stu-id="ebe93-131">INPUTS</span></span>

### <span data-ttu-id="ebe93-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ebe93-132">System.String</span></span>

## <span data-ttu-id="ebe93-133">출력</span><span class="sxs-lookup"><span data-stu-id="ebe93-133">OUTPUTS</span></span>

### <span data-ttu-id="ebe93-134">PSNetAppFilesReplicationStatus-. p m.</span><span class="sxs-lookup"><span data-stu-id="ebe93-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="ebe93-135">상속자</span><span class="sxs-lookup"><span data-stu-id="ebe93-135">NOTES</span></span>

## <span data-ttu-id="ebe93-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ebe93-136">RELATED LINKS</span></span>
