---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 8f64eded908e331e22addfeeb65f74a477c70b54
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876840"
---
# <span data-ttu-id="3ccfa-101">Get-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="3ccfa-101">Get-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="3ccfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ccfa-102">SYNOPSIS</span></span>
<span data-ttu-id="3ccfa-103">사용 가능한 데이터 상자 가장자리 장치에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3ccfa-103">Gets the information on available Data Box Edge devices.</span></span>

## <span data-ttu-id="3ccfa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3ccfa-104">SYNTAX</span></span>

### <span data-ttu-id="3ccfa-105">ListByParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3ccfa-105">ListByParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ccfa-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ccfa-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ccfa-107">GetExtendedInfoByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ccfa-107">GetExtendedInfoByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-ExtendedInfo] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ccfa-108">GetNetworkSettingByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ccfa-108">GetNetworkSettingByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-NetworkSetting] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ccfa-109">GetSummaryUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ccfa-109">GetSummaryUpdateByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ccfa-110">GetAlertByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ccfa-110">GetAlertByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-Alert] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ccfa-111">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ccfa-111">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ccfa-112">GetSummaryUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ccfa-112">GetSummaryUpdateParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ccfa-113">GetNetworkSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ccfa-113">GetNetworkSettingParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-NetworkSetting]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ccfa-114">GetExtendedInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ccfa-114">GetExtendedInfoParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ccfa-115">GetAlertParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ccfa-115">GetAlertParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-Alert]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ccfa-116">설명은</span><span class="sxs-lookup"><span data-stu-id="3ccfa-116">DESCRIPTION</span></span>
<span data-ttu-id="3ccfa-117">**AzDataBoxEdgeDevice** cmdlet은 사용 가능한 데이터 상자 가장자리 장치에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3ccfa-117">The **Get-AzDataBoxEdgeDevice** cmdlet gets the information about the available Data Box Edge Devices.</span></span> <span data-ttu-id="3ccfa-118">리소스 그룹 이름과 함께 디바이스의 이름을 지정 하 여 특정 장치에 대 한 정보를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3ccfa-118">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="3ccfa-119">예제의</span><span class="sxs-lookup"><span data-stu-id="3ccfa-119">EXAMPLES</span></span>

### <span data-ttu-id="3ccfa-120">예제 1</span><span class="sxs-lookup"><span data-stu-id="3ccfa-120">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="3ccfa-121">예제 2</span><span class="sxs-lookup"><span data-stu-id="3ccfa-121">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceId /subscriptions/subscriptionId/resourcegroups/resourceGroupName/providers/Microsoft.DataBoxEdge/dataBoxEdgeDevices/deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

### <span data-ttu-id="3ccfa-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="3ccfa-122">Example 3</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="3ccfa-123">변수</span><span class="sxs-lookup"><span data-stu-id="3ccfa-123">PARAMETERS</span></span>

### <span data-ttu-id="3ccfa-124">-경고</span><span class="sxs-lookup"><span data-stu-id="3ccfa-124">-Alert</span></span>
<span data-ttu-id="3ccfa-125">데이터 상자에 지/게이트웨이 장치에서 알림 가져오기</span><span class="sxs-lookup"><span data-stu-id="3ccfa-125">Fetch the alerts on the data box edge/gateway device</span></span>

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

### <span data-ttu-id="3ccfa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ccfa-126">-DefaultProfile</span></span>
<span data-ttu-id="3ccfa-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3ccfa-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ccfa-128">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="3ccfa-128">-ExtendedInfo</span></span>
<span data-ttu-id="3ccfa-129">지정 된 데이터 상자에 대 한 추가 정보 (Edge/데이터 상자 게이트웨이 장치)를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3ccfa-129">Gets additional information for the specified Data Box Edge/Data Box Gateway device</span></span>

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

### <span data-ttu-id="3ccfa-130">-이름</span><span class="sxs-lookup"><span data-stu-id="3ccfa-130">-Name</span></span>
<span data-ttu-id="3ccfa-131">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3ccfa-131">Resource Group Name</span></span>

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

### <span data-ttu-id="3ccfa-132">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="3ccfa-132">-NetworkSetting</span></span>
<span data-ttu-id="3ccfa-133">지정 된 데이터 상자에 대 한 네트워크 설정 (Edge/데이터 상자 게이트웨이 디바이스)을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3ccfa-133">Gets the network settings of the specified Data Box Edge/Data Box Gateway device</span></span>

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

### <span data-ttu-id="3ccfa-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ccfa-134">-ResourceGroupName</span></span>
<span data-ttu-id="3ccfa-135">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3ccfa-135">Resource Group Name</span></span>

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

### <span data-ttu-id="3ccfa-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ccfa-136">-ResourceId</span></span>
<span data-ttu-id="3ccfa-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ccfa-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="3ccfa-138">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="3ccfa-138">-UpdateSummary</span></span>
<span data-ttu-id="3ccfa-139">장치의 마지막 검사를 기반으로 업데이트의 가용성에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3ccfa-139">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="3ccfa-140">또한 장치에서 진행 중인 모든 다운로드 또는 설치 작업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3ccfa-140">It also gets information about any ongoing download or install jobs on the device.</span></span>

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

### <span data-ttu-id="3ccfa-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ccfa-141">CommonParameters</span></span>
<span data-ttu-id="3ccfa-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ccfa-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ccfa-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3ccfa-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ccfa-144">입력</span><span class="sxs-lookup"><span data-stu-id="3ccfa-144">INPUTS</span></span>

### <span data-ttu-id="3ccfa-145">않아야</span><span class="sxs-lookup"><span data-stu-id="3ccfa-145">None</span></span>

## <span data-ttu-id="3ccfa-146">출력</span><span class="sxs-lookup"><span data-stu-id="3ccfa-146">OUTPUTS</span></span>

### <span data-ttu-id="3ccfa-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="3ccfa-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="3ccfa-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="3ccfa-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span></span>

### <span data-ttu-id="3ccfa-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="3ccfa-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span></span>

### <span data-ttu-id="3ccfa-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span><span class="sxs-lookup"><span data-stu-id="3ccfa-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span></span>

### <span data-ttu-id="3ccfa-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span><span class="sxs-lookup"><span data-stu-id="3ccfa-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span></span>

## <span data-ttu-id="3ccfa-152">상속자</span><span class="sxs-lookup"><span data-stu-id="3ccfa-152">NOTES</span></span>

## <span data-ttu-id="3ccfa-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ccfa-153">RELATED LINKS</span></span>
