---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
ms.openlocfilehash: 14e5bbc222bf92f95d77277c6f8d82f578efd0b3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495459"
---
# <span data-ttu-id="728ad-101">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="728ad-101">Get-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="728ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="728ad-102">SYNOPSIS</span></span>
<span data-ttu-id="728ad-103">지정된 디바이스의 부모 디바이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="728ad-103">Get the parent device of the specified device.</span></span>

## <span data-ttu-id="728ad-104">구문</span><span class="sxs-lookup"><span data-stu-id="728ad-104">SYNTAX</span></span>

### <span data-ttu-id="728ad-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="728ad-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="728ad-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="728ad-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="728ad-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="728ad-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="728ad-108">설명</span><span class="sxs-lookup"><span data-stu-id="728ad-108">DESCRIPTION</span></span>
<span data-ttu-id="728ad-109">지정된 비에지 디바이스의 부모 디바이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="728ad-109">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="728ad-110">예제</span><span class="sxs-lookup"><span data-stu-id="728ad-110">EXAMPLES</span></span>

### <span data-ttu-id="728ad-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="728ad-111">Example 1</span></span>
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

<span data-ttu-id="728ad-112">지정된 비에지 디바이스의 부모 디바이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="728ad-112">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="728ad-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="728ad-113">PARAMETERS</span></span>

### <span data-ttu-id="728ad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="728ad-114">-DefaultProfile</span></span>
<span data-ttu-id="728ad-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="728ad-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="728ad-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="728ad-116">-DeviceId</span></span>
<span data-ttu-id="728ad-117">비에지 디바이스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="728ad-117">Id of non-edge device.</span></span>

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

### <span data-ttu-id="728ad-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="728ad-118">-InputObject</span></span>
<span data-ttu-id="728ad-119">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="728ad-119">IotHub object</span></span>

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

### <span data-ttu-id="728ad-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="728ad-120">-IotHubName</span></span>
<span data-ttu-id="728ad-121">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="728ad-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="728ad-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="728ad-122">-ResourceGroupName</span></span>
<span data-ttu-id="728ad-123">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="728ad-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="728ad-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="728ad-124">-ResourceId</span></span>
<span data-ttu-id="728ad-125">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="728ad-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="728ad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="728ad-126">CommonParameters</span></span>
<span data-ttu-id="728ad-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="728ad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="728ad-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="728ad-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="728ad-129">입력</span><span class="sxs-lookup"><span data-stu-id="728ad-129">INPUTS</span></span>

### <span data-ttu-id="728ad-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="728ad-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="728ad-131">System.String</span><span class="sxs-lookup"><span data-stu-id="728ad-131">System.String</span></span>

## <span data-ttu-id="728ad-132">출력</span><span class="sxs-lookup"><span data-stu-id="728ad-132">OUTPUTS</span></span>

### <span data-ttu-id="728ad-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSD</span><span class="sxs-lookup"><span data-stu-id="728ad-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="728ad-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="728ad-134">NOTES</span></span>

## <span data-ttu-id="728ad-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="728ad-135">RELATED LINKS</span></span>
