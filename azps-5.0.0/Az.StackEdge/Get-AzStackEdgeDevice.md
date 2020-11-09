---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeDevice.md
ms.openlocfilehash: 1fa868d9df41a5f4f995981c332497d9555e1174
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310586"
---
# <span data-ttu-id="e364c-101">Get-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e364c-101">Get-AzStackEdgeDevice</span></span>

## <span data-ttu-id="e364c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e364c-102">SYNOPSIS</span></span>
<span data-ttu-id="e364c-103">사용 가능한 스택 가장자리 장치에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e364c-103">Gets the information on available Stack Edge devices.</span></span>

## <span data-ttu-id="e364c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e364c-104">SYNTAX</span></span>

### <span data-ttu-id="e364c-105">ListByParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e364c-105">ListByParameterSet (Default)</span></span>
```
Get-AzStackEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e364c-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e364c-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeDevice -ResourceId <String> [-ExtendedInfo] [-NetworkSetting] [-Alert] [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e364c-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e364c-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo] [-NetworkSetting] [-Alert]
 [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e364c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e364c-108">DESCRIPTION</span></span>
<span data-ttu-id="e364c-109">**AzStackEdgeDevice** cmdlet은 사용 가능한 스택 경계 장치에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e364c-109">The **Get-AzStackEdgeDevice** cmdlet gets the information about the available Stack Edge Devices.</span></span> <span data-ttu-id="e364c-110">리소스 그룹 이름과 함께 디바이스의 이름을 지정 하 여 특정 장치에 대 한 정보를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e364c-110">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="e364c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e364c-111">EXAMPLES</span></span>

### <span data-ttu-id="e364c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="e364c-112">Example 1</span></span>
```powershell
PS C:\>Get-AzStackEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="e364c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e364c-113">Example 2</span></span>
```powershell
PS C:\>$device = Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName1 -DeviceName deviceNameOne -Alert -UpdateSummary -NetworkSetting -ExtendedInfo

PS C:\>$device.Alert

Title                            Severity AppearedDateTime      Recommendation
-----                            -------- ----------------      --------------
Lost heartbeat from your device. Critical 02-Jan-20 10:35:20 AM If your device is offline, then the device is not able to communicate with the Azure service. This could be due to one of the following reasons: <br/> &nbs�


PS C:\>$device.NetworkSetting

State    IPv4         IPv6                                 Subnet        Default Gateway Physical address DNS Servers
-----    ----         ----                                 ------        --------------- ---------------- -----------
Disabled 10.150.76.82 2404:f801:4800:1e:8168:dca6:b3b9:d70 255.255.252.0 10.150.76.1     00155D4E262B     10.50.50.50,10.50.10.50

PS C:\>$device.UpdateSummary

DeviceName        Current Version Friendly name      Last Software Scan Last Software Update Pending Updates Pending Update Titles
----------        --------------- -------------      ------------------ -------------------- --------------- ---------------------
deviceNameOne     2.0.998.537     Data Box Edge Mock                                         0

PS C:\>$device.ExtendedInfo

ResourceGroupName   DeviceName        EncryptedCIK Thumbprint     ResourceKey        EncryptedCIK
-----------------   ----------        -----------------------     -----------        ------------
resourceGroupName1  deviceNameOne     EncryptedCIKThumbpring      411182691329779166 EncryptedCIK
```

## <span data-ttu-id="e364c-114">변수</span><span class="sxs-lookup"><span data-stu-id="e364c-114">PARAMETERS</span></span>

### <span data-ttu-id="e364c-115">-경고</span><span class="sxs-lookup"><span data-stu-id="e364c-115">-Alert</span></span>
<span data-ttu-id="e364c-116">스택 가장자리/게이트웨이 장치에서 알림 가져오기</span><span class="sxs-lookup"><span data-stu-id="e364c-116">Fetch the alerts on the Stack edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e364c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e364c-117">-DefaultProfile</span></span>
<span data-ttu-id="e364c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e364c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e364c-119">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="e364c-119">-ExtendedInfo</span></span>
<span data-ttu-id="e364c-120">지정 된 스택 경계 또는 스택 게이트웨이 장치에 대 한 추가 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e364c-120">Gets additional information for the specified Stack Edge/Stack Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e364c-121">-이름</span><span class="sxs-lookup"><span data-stu-id="e364c-121">-Name</span></span>
<span data-ttu-id="e364c-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e364c-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e364c-123">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="e364c-123">-NetworkSetting</span></span>
<span data-ttu-id="e364c-124">지정 된 스택 경계 또는 스택 게이트웨이 장치의 네트워크 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e364c-124">Gets the network settings of the specified Stack Edge/Stack Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e364c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e364c-125">-ResourceGroupName</span></span>
<span data-ttu-id="e364c-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e364c-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListByParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e364c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e364c-127">-ResourceId</span></span>
<span data-ttu-id="e364c-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e364c-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e364c-129">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="e364c-129">-UpdateSummary</span></span>
<span data-ttu-id="e364c-130">장치의 마지막 검사를 기반으로 업데이트의 가용성에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e364c-130">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="e364c-131">또한 장치에서 진행 중인 모든 다운로드 또는 설치 작업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e364c-131">It also gets information about any ongoing download or install jobs on the device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByResourceIdParameterSet, GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e364c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e364c-132">CommonParameters</span></span>
<span data-ttu-id="e364c-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e364c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e364c-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e364c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e364c-135">입력</span><span class="sxs-lookup"><span data-stu-id="e364c-135">INPUTS</span></span>

## <span data-ttu-id="e364c-136">출력</span><span class="sxs-lookup"><span data-stu-id="e364c-136">OUTPUTS</span></span>

## <span data-ttu-id="e364c-137">상속자</span><span class="sxs-lookup"><span data-stu-id="e364c-137">NOTES</span></span>

## <span data-ttu-id="e364c-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e364c-138">RELATED LINKS</span></span>
