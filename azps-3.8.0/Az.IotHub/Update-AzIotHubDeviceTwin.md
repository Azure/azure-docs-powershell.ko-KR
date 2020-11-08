---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 16c3ab31959268aa998d50290180d4d8b3231ccf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034613"
---
# <span data-ttu-id="6fc79-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="6fc79-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="6fc79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fc79-102">SYNOPSIS</span></span>
<span data-ttu-id="6fc79-103">장치 트윈의 태그 및 원하는 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc79-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="6fc79-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6fc79-104">SYNTAX</span></span>

### <span data-ttu-id="6fc79-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6fc79-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fc79-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6fc79-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6fc79-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6fc79-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fc79-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6fc79-108">DESCRIPTION</span></span>
<span data-ttu-id="6fc79-109">장치 트윈을 업데이트 하거나 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="6fc79-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="6fc79-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins자세한 내용은을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6fc79-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="6fc79-111">예제의</span><span class="sxs-lookup"><span data-stu-id="6fc79-111">EXAMPLES</span></span>

### <span data-ttu-id="6fc79-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="6fc79-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="6fc79-113">업데이트 된 장치 트윈 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc79-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="6fc79-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="6fc79-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="6fc79-115">업데이트 된 원하는 속성이 있는 디바이스 트윈 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc79-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="6fc79-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="6fc79-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="6fc79-117">업데이트 된 태그 속성이 있는 디바이스 트윈 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc79-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="6fc79-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="6fc79-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="6fc79-119">대체 된 장치 트윈 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc79-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="6fc79-120">변수</span><span class="sxs-lookup"><span data-stu-id="6fc79-120">PARAMETERS</span></span>

### <span data-ttu-id="6fc79-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fc79-121">-DefaultProfile</span></span>
<span data-ttu-id="6fc79-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6fc79-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fc79-123">-원하는</span><span class="sxs-lookup"><span data-stu-id="6fc79-123">-Desired</span></span>
<span data-ttu-id="6fc79-124">장치 트윈에서 원하는 속성을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc79-124">Add or update the desired property in a device twin.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fc79-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="6fc79-125">-DeviceId</span></span>
<span data-ttu-id="6fc79-126">대상 장치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="6fc79-126">Target Device Id.</span></span>

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

### <span data-ttu-id="6fc79-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fc79-127">-InputObject</span></span>
<span data-ttu-id="6fc79-128">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="6fc79-128">IotHub object</span></span>

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

### <span data-ttu-id="6fc79-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6fc79-129">-IotHubName</span></span>
<span data-ttu-id="6fc79-130">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="6fc79-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6fc79-131">-부분</span><span class="sxs-lookup"><span data-stu-id="6fc79-131">-Partial</span></span>
<span data-ttu-id="6fc79-132">장치 트윈의 태그 및 원하는 속성을 부분적 으로만 업데이트 하도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc79-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="6fc79-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fc79-133">-ResourceGroupName</span></span>
<span data-ttu-id="6fc79-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6fc79-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6fc79-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fc79-135">-ResourceId</span></span>
<span data-ttu-id="6fc79-136">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="6fc79-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6fc79-137">태그</span><span class="sxs-lookup"><span data-stu-id="6fc79-137">-Tag</span></span>
<span data-ttu-id="6fc79-138">장치 트윈에서 tags 속성을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc79-138">Add or update the tags property in a device twin.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fc79-139">-확인</span><span class="sxs-lookup"><span data-stu-id="6fc79-139">-Confirm</span></span>
<span data-ttu-id="6fc79-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc79-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fc79-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fc79-141">-WhatIf</span></span>
<span data-ttu-id="6fc79-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6fc79-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fc79-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6fc79-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fc79-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fc79-144">CommonParameters</span></span>
<span data-ttu-id="6fc79-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc79-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fc79-146">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fc79-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fc79-147">입력</span><span class="sxs-lookup"><span data-stu-id="6fc79-147">INPUTS</span></span>

### <span data-ttu-id="6fc79-148">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="6fc79-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6fc79-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6fc79-149">System.String</span></span>

## <span data-ttu-id="6fc79-150">출력</span><span class="sxs-lookup"><span data-stu-id="6fc79-150">OUTPUTS</span></span>

### <span data-ttu-id="6fc79-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6fc79-151">System.String</span></span>

## <span data-ttu-id="6fc79-152">상속자</span><span class="sxs-lookup"><span data-stu-id="6fc79-152">NOTES</span></span>

## <span data-ttu-id="6fc79-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6fc79-153">RELATED LINKS</span></span>
