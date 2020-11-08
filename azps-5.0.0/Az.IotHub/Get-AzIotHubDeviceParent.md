---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
ms.openlocfilehash: 14e5bbc222bf92f95d77277c6f8d82f578efd0b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217750"
---
# <span data-ttu-id="ea6a8-101">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="ea6a8-101">Get-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="ea6a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea6a8-102">SYNOPSIS</span></span>
<span data-ttu-id="ea6a8-103">지정 된 장치의 부모 장치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ea6a8-103">Get the parent device of the specified device.</span></span>

## <span data-ttu-id="ea6a8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea6a8-104">SYNTAX</span></span>

### <span data-ttu-id="ea6a8-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ea6a8-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea6a8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ea6a8-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea6a8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ea6a8-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea6a8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ea6a8-108">DESCRIPTION</span></span>
<span data-ttu-id="ea6a8-109">지정 된 비 경계 장치의 부모 장치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ea6a8-109">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="ea6a8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ea6a8-110">EXAMPLES</span></span>

### <span data-ttu-id="ea6a8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ea6a8-111">Example 1</span></span>
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

<span data-ttu-id="ea6a8-112">지정 된 비 경계 장치의 부모 장치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ea6a8-112">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="ea6a8-113">변수</span><span class="sxs-lookup"><span data-stu-id="ea6a8-113">PARAMETERS</span></span>

### <span data-ttu-id="ea6a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea6a8-114">-DefaultProfile</span></span>
<span data-ttu-id="ea6a8-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea6a8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea6a8-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="ea6a8-116">-DeviceId</span></span>
<span data-ttu-id="ea6a8-117">비 경계 디바이스의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="ea6a8-117">Id of non-edge device.</span></span>

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

### <span data-ttu-id="ea6a8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea6a8-118">-InputObject</span></span>
<span data-ttu-id="ea6a8-119">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="ea6a8-119">IotHub object</span></span>

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

### <span data-ttu-id="ea6a8-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ea6a8-120">-IotHubName</span></span>
<span data-ttu-id="ea6a8-121">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="ea6a8-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ea6a8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea6a8-122">-ResourceGroupName</span></span>
<span data-ttu-id="ea6a8-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea6a8-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ea6a8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea6a8-124">-ResourceId</span></span>
<span data-ttu-id="ea6a8-125">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="ea6a8-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ea6a8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea6a8-126">CommonParameters</span></span>
<span data-ttu-id="ea6a8-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea6a8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea6a8-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea6a8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea6a8-129">입력</span><span class="sxs-lookup"><span data-stu-id="ea6a8-129">INPUTS</span></span>

### <span data-ttu-id="ea6a8-130">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="ea6a8-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ea6a8-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ea6a8-131">System.String</span></span>

## <span data-ttu-id="ea6a8-132">출력</span><span class="sxs-lookup"><span data-stu-id="ea6a8-132">OUTPUTS</span></span>

### <span data-ttu-id="ea6a8-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="ea6a8-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="ea6a8-134">상속자</span><span class="sxs-lookup"><span data-stu-id="ea6a8-134">NOTES</span></span>

## <span data-ttu-id="ea6a8-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea6a8-135">RELATED LINKS</span></span>
