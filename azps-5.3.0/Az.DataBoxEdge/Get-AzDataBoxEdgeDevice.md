---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 314ebb4412b88e5476a63cf5a1025f26e2c41e69
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493612"
---
# <span data-ttu-id="77e47-101">Get-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="77e47-101">Get-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="77e47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77e47-102">SYNOPSIS</span></span>
<span data-ttu-id="77e47-103">사용 가능한 Data Box Edge 디바이스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="77e47-103">Gets the information on available Data Box Edge devices.</span></span>

## <span data-ttu-id="77e47-104">구문</span><span class="sxs-lookup"><span data-stu-id="77e47-104">SYNTAX</span></span>

### <span data-ttu-id="77e47-105">ListByParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="77e47-105">ListByParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="77e47-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77e47-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77e47-107">GetExtendedInfoByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77e47-107">GetExtendedInfoByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-ExtendedInfo] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="77e47-108">GetNetworkSettingByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77e47-108">GetNetworkSettingByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-NetworkSetting] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="77e47-109">GetSummaryUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77e47-109">GetSummaryUpdateByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="77e47-110">GetAlertByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77e47-110">GetAlertByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-Alert] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="77e47-111">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="77e47-111">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77e47-112">GetSummaryUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="77e47-112">GetSummaryUpdateParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77e47-113">GetNetworkSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="77e47-113">GetNetworkSettingParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-NetworkSetting]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77e47-114">GetExtendedInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="77e47-114">GetExtendedInfoParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77e47-115">GetAlertParameterSet</span><span class="sxs-lookup"><span data-stu-id="77e47-115">GetAlertParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-Alert]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77e47-116">설명</span><span class="sxs-lookup"><span data-stu-id="77e47-116">DESCRIPTION</span></span>
<span data-ttu-id="77e47-117">**Get-AzDataBoxEdgeDevice** cmdlet은 사용 가능한 Data Box Edge 디바이스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="77e47-117">The **Get-AzDataBoxEdgeDevice** cmdlet gets the information about the available Data Box Edge Devices.</span></span> <span data-ttu-id="77e47-118">리소스 그룹 이름과 함께 디바이스 이름을 지정하여 특정 디바이스에 대한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77e47-118">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="77e47-119">예제</span><span class="sxs-lookup"><span data-stu-id="77e47-119">EXAMPLES</span></span>

### <span data-ttu-id="77e47-120">예제 1</span><span class="sxs-lookup"><span data-stu-id="77e47-120">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="77e47-121">예제 2</span><span class="sxs-lookup"><span data-stu-id="77e47-121">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceId /subscriptions/subscriptionId/resourcegroups/resourceGroupName/providers/Microsoft.DataBoxEdge/dataBoxEdgeDevices/deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

### <span data-ttu-id="77e47-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="77e47-122">Example 3</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="77e47-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77e47-123">PARAMETERS</span></span>

### <span data-ttu-id="77e47-124">-Alert</span><span class="sxs-lookup"><span data-stu-id="77e47-124">-Alert</span></span>
<span data-ttu-id="77e47-125">데이터 상자 에지/게이트웨이 디바이스에서 경고를 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="77e47-125">Fetch the alerts on the data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAlertByResourceIdParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e47-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77e47-126">-DefaultProfile</span></span>
<span data-ttu-id="77e47-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77e47-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77e47-128">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="77e47-128">-ExtendedInfo</span></span>
<span data-ttu-id="77e47-129">지정된 Data Box Edge/Data Box Gateway 디바이스에 대한 추가 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="77e47-129">Gets additional information for the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetExtendedInfoByResourceIdParameterSet, GetExtendedInfoParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e47-130">-Name</span><span class="sxs-lookup"><span data-stu-id="77e47-130">-Name</span></span>
<span data-ttu-id="77e47-131">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="77e47-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e47-132">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="77e47-132">-NetworkSetting</span></span>
<span data-ttu-id="77e47-133">지정된 Data Box Edge/Data Box Gateway 디바이스의 네트워크 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="77e47-133">Gets the network settings of the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNetworkSettingByResourceIdParameterSet, GetNetworkSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e47-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77e47-134">-ResourceGroupName</span></span>
<span data-ttu-id="77e47-135">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="77e47-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListByParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e47-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77e47-136">-ResourceId</span></span>
<span data-ttu-id="77e47-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="77e47-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet, GetExtendedInfoByResourceIdParameterSet, GetNetworkSettingByResourceIdParameterSet, GetSummaryUpdateByResourceIdParameterSet, GetAlertByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e47-138">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="77e47-138">-UpdateSummary</span></span>
<span data-ttu-id="77e47-139">디바이스의 마지막 검사에 따라 업데이트의 가용성에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="77e47-139">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="77e47-140">또한 디바이스에서 진행되는 다운로드 또는 설치 작업 관련 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="77e47-140">It also gets information about any ongoing download or install jobs on the device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetSummaryUpdateByResourceIdParameterSet, GetSummaryUpdateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e47-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77e47-141">CommonParameters</span></span>
<span data-ttu-id="77e47-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="77e47-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77e47-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="77e47-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77e47-144">입력</span><span class="sxs-lookup"><span data-stu-id="77e47-144">INPUTS</span></span>

### <span data-ttu-id="77e47-145">없음</span><span class="sxs-lookup"><span data-stu-id="77e47-145">None</span></span>

## <span data-ttu-id="77e47-146">출력</span><span class="sxs-lookup"><span data-stu-id="77e47-146">OUTPUTS</span></span>

### <span data-ttu-id="77e47-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="77e47-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="77e47-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="77e47-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span></span>

### <span data-ttu-id="77e47-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="77e47-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span></span>

### <span data-ttu-id="77e47-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span><span class="sxs-lookup"><span data-stu-id="77e47-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span></span>

### <span data-ttu-id="77e47-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span><span class="sxs-lookup"><span data-stu-id="77e47-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span></span>

## <span data-ttu-id="77e47-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="77e47-152">NOTES</span></span>

## <span data-ttu-id="77e47-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77e47-153">RELATED LINKS</span></span>
