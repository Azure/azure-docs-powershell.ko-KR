---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
ms.openlocfilehash: 834a7444cda059614a7aa8b96acf99ba9cacd336
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968512"
---
# <span data-ttu-id="69db1-101">Get-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="69db1-101">Get-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="69db1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69db1-102">SYNOPSIS</span></span>
<span data-ttu-id="69db1-103">ANF(Azure NetApp Files) 볼륨에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="69db1-103">Gets details of an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="69db1-104">구문</span><span class="sxs-lookup"><span data-stu-id="69db1-104">SYNTAX</span></span>

### <span data-ttu-id="69db1-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="69db1-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69db1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69db1-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVolume -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69db1-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69db1-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVolume -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69db1-108">설명</span><span class="sxs-lookup"><span data-stu-id="69db1-108">DESCRIPTION</span></span>
<span data-ttu-id="69db1-109">**Get-AzNetAppFilesVolume** cmdlet은 ANF 볼륨에 대한 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="69db1-109">The **Get-AzNetAppFilesVolume** cmdlet gets details of an ANF volume.</span></span>

## <span data-ttu-id="69db1-110">예제</span><span class="sxs-lookup"><span data-stu-id="69db1-110">EXAMPLES</span></span>

### <span data-ttu-id="69db1-111">예제 1: ANF 볼륨을 얻다</span><span class="sxs-lookup"><span data-stu-id="69db1-111">Example 1: Get an ANF volume</span></span>
```
PS C:\>Get-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     :
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="69db1-112">이 명령은 풀 "MyAnfPool"에서 MyAnfVolume이라는 볼륨을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="69db1-112">This command gets the volume named MyAnfVolume from the pool "MyAnfPool".</span></span> 

## <span data-ttu-id="69db1-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="69db1-113">PARAMETERS</span></span>

### <span data-ttu-id="69db1-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="69db1-114">-AccountName</span></span>
<span data-ttu-id="69db1-115">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="69db1-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="69db1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69db1-116">-DefaultProfile</span></span>
<span data-ttu-id="69db1-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69db1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69db1-118">-Name</span><span class="sxs-lookup"><span data-stu-id="69db1-118">-Name</span></span>
<span data-ttu-id="69db1-119">ANF 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="69db1-119">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69db1-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="69db1-120">-PoolName</span></span>
<span data-ttu-id="69db1-121">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="69db1-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="69db1-122">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="69db1-122">-PoolObject</span></span>
<span data-ttu-id="69db1-123">반환할 볼륨을 포함하는 풀 개체</span><span class="sxs-lookup"><span data-stu-id="69db1-123">The pool object containing the volume to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69db1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69db1-124">-ResourceGroupName</span></span>
<span data-ttu-id="69db1-125">ANF 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="69db1-125">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="69db1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69db1-126">-ResourceId</span></span>
<span data-ttu-id="69db1-127">ANF 볼륨의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="69db1-127">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="69db1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69db1-128">CommonParameters</span></span>
<span data-ttu-id="69db1-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="69db1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69db1-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69db1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69db1-131">입력</span><span class="sxs-lookup"><span data-stu-id="69db1-131">INPUTS</span></span>

### <span data-ttu-id="69db1-132">System.String</span><span class="sxs-lookup"><span data-stu-id="69db1-132">System.String</span></span>

### <span data-ttu-id="69db1-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="69db1-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="69db1-134">출력</span><span class="sxs-lookup"><span data-stu-id="69db1-134">OUTPUTS</span></span>

### <span data-ttu-id="69db1-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="69db1-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="69db1-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="69db1-136">NOTES</span></span>

## <span data-ttu-id="69db1-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69db1-137">RELATED LINKS</span></span>
