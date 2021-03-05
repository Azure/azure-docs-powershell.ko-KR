---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
ms.openlocfilehash: 06eb84ea854e9c0262f6f3e00e3e13e90f630baa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988059"
---
# <span data-ttu-id="cb06c-101">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="cb06c-101">Get-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="cb06c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb06c-102">SYNOPSIS</span></span>
<span data-ttu-id="cb06c-103">지정된 디바이스의 상위 디바이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb06c-103">Get the parent device of the specified device.</span></span>

## <span data-ttu-id="cb06c-104">구문</span><span class="sxs-lookup"><span data-stu-id="cb06c-104">SYNTAX</span></span>

### <span data-ttu-id="cb06c-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="cb06c-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb06c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cb06c-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb06c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cb06c-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cb06c-108">설명</span><span class="sxs-lookup"><span data-stu-id="cb06c-108">DESCRIPTION</span></span>
<span data-ttu-id="cb06c-109">지정된 비에지 디바이스의 부모 디바이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb06c-109">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="cb06c-110">예제</span><span class="sxs-lookup"><span data-stu-id="cb06c-110">EXAMPLES</span></span>

### <span data-ttu-id="cb06c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cb06c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId                   : myParentDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Enabled
StatusReason               : 
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : True
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

<span data-ttu-id="cb06c-112">지정된 비에지 디바이스의 부모 디바이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb06c-112">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="cb06c-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cb06c-113">PARAMETERS</span></span>

### <span data-ttu-id="cb06c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb06c-114">-DefaultProfile</span></span>
<span data-ttu-id="cb06c-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb06c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb06c-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="cb06c-116">-DeviceId</span></span>
<span data-ttu-id="cb06c-117">비에지 디바이스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cb06c-117">Id of non-edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb06c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb06c-118">-InputObject</span></span>
<span data-ttu-id="cb06c-119">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="cb06c-119">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb06c-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="cb06c-120">-IotHubName</span></span>
<span data-ttu-id="cb06c-121">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="cb06c-121">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb06c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb06c-122">-ResourceGroupName</span></span>
<span data-ttu-id="cb06c-123">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="cb06c-123">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb06c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb06c-124">-ResourceId</span></span>
<span data-ttu-id="cb06c-125">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="cb06c-125">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb06c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb06c-126">CommonParameters</span></span>
<span data-ttu-id="cb06c-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb06c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb06c-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb06c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb06c-129">입력</span><span class="sxs-lookup"><span data-stu-id="cb06c-129">INPUTS</span></span>

### <span data-ttu-id="cb06c-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="cb06c-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="cb06c-131">System.String</span><span class="sxs-lookup"><span data-stu-id="cb06c-131">System.String</span></span>

## <span data-ttu-id="cb06c-132">출력</span><span class="sxs-lookup"><span data-stu-id="cb06c-132">OUTPUTS</span></span>

### <span data-ttu-id="cb06c-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSD에비스</span><span class="sxs-lookup"><span data-stu-id="cb06c-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="cb06c-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cb06c-134">NOTES</span></span>

## <span data-ttu-id="cb06c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb06c-135">RELATED LINKS</span></span>
