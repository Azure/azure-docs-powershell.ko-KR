---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 80d8a27aaf0d2aa27f9924d93669548c1d0dda93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968592"
---
# <span data-ttu-id="40826-101">Get-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="40826-101">Get-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="40826-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40826-102">SYNOPSIS</span></span>
<span data-ttu-id="40826-103">ANF(Azure NetApp Files) 스냅숏에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="40826-103">Gets details of an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="40826-104">구문</span><span class="sxs-lookup"><span data-stu-id="40826-104">SYNTAX</span></span>

### <span data-ttu-id="40826-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="40826-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40826-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40826-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="40826-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40826-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40826-108">설명</span><span class="sxs-lookup"><span data-stu-id="40826-108">DESCRIPTION</span></span>
<span data-ttu-id="40826-109">**Get-AzNetAppFilesSnapshot** cmdlet은 ANF 스냅숏에 대한 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="40826-109">The **Get-AzNetAppFilesSnapshot** cmdlet gets details of an ANF snapshot.</span></span>

## <span data-ttu-id="40826-110">예제</span><span class="sxs-lookup"><span data-stu-id="40826-110">EXAMPLES</span></span>

### <span data-ttu-id="40826-111">예제 1: ANF 스냅숏 만들기</span><span class="sxs-lookup"><span data-stu-id="40826-111">Example 1: Get an ANF snapshot</span></span>
```
PS C:\>Get-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="40826-112">이 명령은 볼륨 "MyAnfVolume"에서 MyAnfSnapshot이라는 스냅숏을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="40826-112">This command gets the snapshot named MyAnfSnapshot from the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="40826-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="40826-113">PARAMETERS</span></span>

### <span data-ttu-id="40826-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="40826-114">-AccountName</span></span>
<span data-ttu-id="40826-115">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="40826-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="40826-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40826-116">-DefaultProfile</span></span>
<span data-ttu-id="40826-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40826-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40826-118">-Name</span><span class="sxs-lookup"><span data-stu-id="40826-118">-Name</span></span>
<span data-ttu-id="40826-119">ANF 스냅숏의 이름</span><span class="sxs-lookup"><span data-stu-id="40826-119">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40826-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="40826-120">-PoolName</span></span>
<span data-ttu-id="40826-121">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="40826-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="40826-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40826-122">-ResourceGroupName</span></span>
<span data-ttu-id="40826-123">ANF 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="40826-123">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="40826-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40826-124">-ResourceId</span></span>
<span data-ttu-id="40826-125">ANF 스냅숏의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="40826-125">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="40826-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="40826-126">-VolumeName</span></span>
<span data-ttu-id="40826-127">ANF 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="40826-127">The name of the ANF volume</span></span>

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

### <span data-ttu-id="40826-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="40826-128">-VolumeObject</span></span>
<span data-ttu-id="40826-129">반환할 스냅숏을 포함하는 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="40826-129">The volume object containing the snapshot to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40826-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40826-130">CommonParameters</span></span>
<span data-ttu-id="40826-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="40826-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40826-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40826-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40826-133">입력</span><span class="sxs-lookup"><span data-stu-id="40826-133">INPUTS</span></span>

### <span data-ttu-id="40826-134">System.String</span><span class="sxs-lookup"><span data-stu-id="40826-134">System.String</span></span>

### <span data-ttu-id="40826-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="40826-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="40826-136">출력</span><span class="sxs-lookup"><span data-stu-id="40826-136">OUTPUTS</span></span>

### <span data-ttu-id="40826-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="40826-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="40826-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="40826-138">NOTES</span></span>

## <span data-ttu-id="40826-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40826-139">RELATED LINKS</span></span>
