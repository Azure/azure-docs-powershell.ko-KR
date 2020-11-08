---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 314ebb4412b88e5476a63cf5a1025f26e2c41e69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94215056"
---
# <span data-ttu-id="65cab-101">Get-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="65cab-101">Get-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="65cab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65cab-102">SYNOPSIS</span></span>
<span data-ttu-id="65cab-103">사용 가능한 데이터 상자 가장자리 장치에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65cab-103">Gets the information on available Data Box Edge devices.</span></span>

## <span data-ttu-id="65cab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="65cab-104">SYNTAX</span></span>

### <span data-ttu-id="65cab-105">ListByParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="65cab-105">ListByParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65cab-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65cab-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65cab-107">GetExtendedInfoByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65cab-107">GetExtendedInfoByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-ExtendedInfo] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65cab-108">GetNetworkSettingByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65cab-108">GetNetworkSettingByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-NetworkSetting] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65cab-109">GetSummaryUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65cab-109">GetSummaryUpdateByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65cab-110">GetAlertByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65cab-110">GetAlertByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-Alert] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65cab-111">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="65cab-111">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65cab-112">GetSummaryUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="65cab-112">GetSummaryUpdateParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65cab-113">GetNetworkSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="65cab-113">GetNetworkSettingParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-NetworkSetting]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65cab-114">GetExtendedInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="65cab-114">GetExtendedInfoParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65cab-115">GetAlertParameterSet</span><span class="sxs-lookup"><span data-stu-id="65cab-115">GetAlertParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-Alert]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65cab-116">설명은</span><span class="sxs-lookup"><span data-stu-id="65cab-116">DESCRIPTION</span></span>
<span data-ttu-id="65cab-117">**AzDataBoxEdgeDevice** cmdlet은 사용 가능한 데이터 상자 가장자리 장치에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65cab-117">The **Get-AzDataBoxEdgeDevice** cmdlet gets the information about the available Data Box Edge Devices.</span></span> <span data-ttu-id="65cab-118">리소스 그룹 이름과 함께 디바이스의 이름을 지정 하 여 특정 장치에 대 한 정보를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65cab-118">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="65cab-119">예제의</span><span class="sxs-lookup"><span data-stu-id="65cab-119">EXAMPLES</span></span>

### <span data-ttu-id="65cab-120">예제 1</span><span class="sxs-lookup"><span data-stu-id="65cab-120">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="65cab-121">예제 2</span><span class="sxs-lookup"><span data-stu-id="65cab-121">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceId /subscriptions/subscriptionId/resourcegroups/resourceGroupName/providers/Microsoft.DataBoxEdge/dataBoxEdgeDevices/deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

### <span data-ttu-id="65cab-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="65cab-122">Example 3</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="65cab-123">변수</span><span class="sxs-lookup"><span data-stu-id="65cab-123">PARAMETERS</span></span>

### <span data-ttu-id="65cab-124">-경고</span><span class="sxs-lookup"><span data-stu-id="65cab-124">-Alert</span></span>
<span data-ttu-id="65cab-125">데이터 상자에 지/게이트웨이 장치에서 알림 가져오기</span><span class="sxs-lookup"><span data-stu-id="65cab-125">Fetch the alerts on the data box edge/gateway device</span></span>

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

### <span data-ttu-id="65cab-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65cab-126">-DefaultProfile</span></span>
<span data-ttu-id="65cab-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65cab-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65cab-128">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="65cab-128">-ExtendedInfo</span></span>
<span data-ttu-id="65cab-129">지정 된 데이터 상자에 대 한 추가 정보 (Edge/데이터 상자 게이트웨이 장치)를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65cab-129">Gets additional information for the specified Data Box Edge/Data Box Gateway device</span></span>

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

### <span data-ttu-id="65cab-130">-이름</span><span class="sxs-lookup"><span data-stu-id="65cab-130">-Name</span></span>
<span data-ttu-id="65cab-131">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="65cab-131">Resource Group Name</span></span>

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

### <span data-ttu-id="65cab-132">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="65cab-132">-NetworkSetting</span></span>
<span data-ttu-id="65cab-133">지정 된 데이터 상자에 대 한 네트워크 설정 (Edge/데이터 상자 게이트웨이 디바이스)을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65cab-133">Gets the network settings of the specified Data Box Edge/Data Box Gateway device</span></span>

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

### <span data-ttu-id="65cab-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65cab-134">-ResourceGroupName</span></span>
<span data-ttu-id="65cab-135">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="65cab-135">Resource Group Name</span></span>

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

### <span data-ttu-id="65cab-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65cab-136">-ResourceId</span></span>
<span data-ttu-id="65cab-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="65cab-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="65cab-138">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="65cab-138">-UpdateSummary</span></span>
<span data-ttu-id="65cab-139">장치의 마지막 검사를 기반으로 업데이트의 가용성에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65cab-139">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="65cab-140">또한 장치에서 진행 중인 모든 다운로드 또는 설치 작업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65cab-140">It also gets information about any ongoing download or install jobs on the device.</span></span>

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

### <span data-ttu-id="65cab-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65cab-141">CommonParameters</span></span>
<span data-ttu-id="65cab-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65cab-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65cab-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="65cab-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65cab-144">입력</span><span class="sxs-lookup"><span data-stu-id="65cab-144">INPUTS</span></span>

### <span data-ttu-id="65cab-145">않아야</span><span class="sxs-lookup"><span data-stu-id="65cab-145">None</span></span>

## <span data-ttu-id="65cab-146">출력</span><span class="sxs-lookup"><span data-stu-id="65cab-146">OUTPUTS</span></span>

### <span data-ttu-id="65cab-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="65cab-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="65cab-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="65cab-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span></span>

### <span data-ttu-id="65cab-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="65cab-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span></span>

### <span data-ttu-id="65cab-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span><span class="sxs-lookup"><span data-stu-id="65cab-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span></span>

### <span data-ttu-id="65cab-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span><span class="sxs-lookup"><span data-stu-id="65cab-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span></span>

## <span data-ttu-id="65cab-152">상속자</span><span class="sxs-lookup"><span data-stu-id="65cab-152">NOTES</span></span>

## <span data-ttu-id="65cab-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65cab-153">RELATED LINKS</span></span>
