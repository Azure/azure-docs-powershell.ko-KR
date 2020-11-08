---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: 1ad24866b4e0403693ace7b53b17271786f218d1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034877"
---
# <span data-ttu-id="e6c80-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="e6c80-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="e6c80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6c80-102">SYNOPSIS</span></span>
<span data-ttu-id="e6c80-103">지정 된 장치의 부모 장치를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c80-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="e6c80-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e6c80-104">SYNTAX</span></span>

### <span data-ttu-id="e6c80-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e6c80-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6c80-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e6c80-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6c80-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e6c80-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6c80-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e6c80-108">DESCRIPTION</span></span>
<span data-ttu-id="e6c80-109">지정 된 비 경계 장치의 부모 장치를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c80-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="e6c80-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e6c80-110">EXAMPLES</span></span>

### <span data-ttu-id="e6c80-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e6c80-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ParentDeviceId "myParentDevice1"

DeviceId                   : myDevice1
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
EdgeEnabled                : False
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

## <span data-ttu-id="e6c80-112">변수</span><span class="sxs-lookup"><span data-stu-id="e6c80-112">PARAMETERS</span></span>

### <span data-ttu-id="e6c80-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6c80-113">-DefaultProfile</span></span>
<span data-ttu-id="e6c80-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e6c80-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6c80-115">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e6c80-115">-DeviceId</span></span>
<span data-ttu-id="e6c80-116">비 경계 디바이스의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="e6c80-116">Id of non-edge device.</span></span>

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

### <span data-ttu-id="e6c80-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e6c80-117">-Force</span></span>
<span data-ttu-id="e6c80-118">비 경계 장치의 상위 장치를 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="e6c80-118">Overwrites the non-edge device's parent device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c80-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6c80-119">-InputObject</span></span>
<span data-ttu-id="e6c80-120">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="e6c80-120">IotHub object</span></span>

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

### <span data-ttu-id="e6c80-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e6c80-121">-IotHubName</span></span>
<span data-ttu-id="e6c80-122">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="e6c80-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e6c80-123">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="e6c80-123">-ParentDeviceId</span></span>
<span data-ttu-id="e6c80-124">Edge 디바이스의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="e6c80-124">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c80-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6c80-125">-ResourceGroupName</span></span>
<span data-ttu-id="e6c80-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6c80-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e6c80-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6c80-127">-ResourceId</span></span>
<span data-ttu-id="e6c80-128">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="e6c80-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e6c80-129">-확인</span><span class="sxs-lookup"><span data-stu-id="e6c80-129">-Confirm</span></span>
<span data-ttu-id="e6c80-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c80-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c80-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6c80-131">-WhatIf</span></span>
<span data-ttu-id="e6c80-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e6c80-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6c80-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6c80-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c80-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6c80-134">CommonParameters</span></span>
<span data-ttu-id="e6c80-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6c80-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6c80-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6c80-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6c80-137">입력</span><span class="sxs-lookup"><span data-stu-id="e6c80-137">INPUTS</span></span>

### <span data-ttu-id="e6c80-138">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="e6c80-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e6c80-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e6c80-139">System.String</span></span>

## <span data-ttu-id="e6c80-140">출력</span><span class="sxs-lookup"><span data-stu-id="e6c80-140">OUTPUTS</span></span>

### <span data-ttu-id="e6c80-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="e6c80-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="e6c80-142">상속자</span><span class="sxs-lookup"><span data-stu-id="e6c80-142">NOTES</span></span>

## <span data-ttu-id="e6c80-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6c80-143">RELATED LINKS</span></span>
