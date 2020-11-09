---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: fb2b984453f87422d7a5b9ec5d5178ca6b6c55d5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304646"
---
# <span data-ttu-id="eb1f2-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="eb1f2-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="eb1f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb1f2-102">SYNOPSIS</span></span>
<span data-ttu-id="eb1f2-103">IoT 장치 모듈 트윈의 태그 및 원하는 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb1f2-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="eb1f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eb1f2-104">SYNTAX</span></span>

### <span data-ttu-id="eb1f2-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="eb1f2-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb1f2-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="eb1f2-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb1f2-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="eb1f2-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb1f2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="eb1f2-108">DESCRIPTION</span></span>
<span data-ttu-id="eb1f2-109">장치 트윈을 업데이트 하거나 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="eb1f2-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="eb1f2-110"> https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins자세한 내용은을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eb1f2-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="eb1f2-111">예제의</span><span class="sxs-lookup"><span data-stu-id="eb1f2-111">EXAMPLES</span></span>

### <span data-ttu-id="eb1f2-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="eb1f2-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="eb1f2-113">업데이트 된 장치 모듈 트윈 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb1f2-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="eb1f2-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="eb1f2-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="eb1f2-115">업데이트 된 속성을 사용 하 여 디바이스 모듈의 트윈 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb1f2-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="eb1f2-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="eb1f2-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="eb1f2-117">업데이트 된 태그 속성이 있는 디바이스 모듈 트윈 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb1f2-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="eb1f2-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="eb1f2-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="eb1f2-119">대체 된 장치 모듈의 트윈 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb1f2-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="eb1f2-120">변수</span><span class="sxs-lookup"><span data-stu-id="eb1f2-120">PARAMETERS</span></span>

### <span data-ttu-id="eb1f2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb1f2-121">-DefaultProfile</span></span>
<span data-ttu-id="eb1f2-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eb1f2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb1f2-123">-원하는</span><span class="sxs-lookup"><span data-stu-id="eb1f2-123">-Desired</span></span>
<span data-ttu-id="eb1f2-124">모듈 트윈에서 원하는 속성을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb1f2-124">Add or update the desired property in a module twin.</span></span>

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

### <span data-ttu-id="eb1f2-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="eb1f2-125">-DeviceId</span></span>
<span data-ttu-id="eb1f2-126">대상 장치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="eb1f2-126">Target Device Id.</span></span>

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

### <span data-ttu-id="eb1f2-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb1f2-127">-InputObject</span></span>
<span data-ttu-id="eb1f2-128">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="eb1f2-128">IotHub object</span></span>

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

### <span data-ttu-id="eb1f2-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="eb1f2-129">-IotHubName</span></span>
<span data-ttu-id="eb1f2-130">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="eb1f2-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="eb1f2-131">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="eb1f2-131">-ModuleId</span></span>
<span data-ttu-id="eb1f2-132">대상 모듈 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="eb1f2-132">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb1f2-133">-부분</span><span class="sxs-lookup"><span data-stu-id="eb1f2-133">-Partial</span></span>
<span data-ttu-id="eb1f2-134">모듈 트윈의 태그 및 원하는 속성만 부분적 으로만 업데이트 하도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb1f2-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="eb1f2-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb1f2-135">-ResourceGroupName</span></span>
<span data-ttu-id="eb1f2-136">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb1f2-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="eb1f2-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb1f2-137">-ResourceId</span></span>
<span data-ttu-id="eb1f2-138">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="eb1f2-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="eb1f2-139">태그</span><span class="sxs-lookup"><span data-stu-id="eb1f2-139">-Tag</span></span>
<span data-ttu-id="eb1f2-140">모듈 트윈에서 tags 속성을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb1f2-140">Add or update the tags property in a module twin.</span></span>

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

### <span data-ttu-id="eb1f2-141">-확인</span><span class="sxs-lookup"><span data-stu-id="eb1f2-141">-Confirm</span></span>
<span data-ttu-id="eb1f2-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb1f2-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb1f2-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb1f2-143">-WhatIf</span></span>
<span data-ttu-id="eb1f2-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eb1f2-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb1f2-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eb1f2-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb1f2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb1f2-146">CommonParameters</span></span>
<span data-ttu-id="eb1f2-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb1f2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb1f2-148">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb1f2-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb1f2-149">입력</span><span class="sxs-lookup"><span data-stu-id="eb1f2-149">INPUTS</span></span>

### <span data-ttu-id="eb1f2-150">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="eb1f2-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="eb1f2-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eb1f2-151">System.String</span></span>

## <span data-ttu-id="eb1f2-152">출력</span><span class="sxs-lookup"><span data-stu-id="eb1f2-152">OUTPUTS</span></span>

### <span data-ttu-id="eb1f2-153">IotHub. PSModuleTwin/. \*</span><span class="sxs-lookup"><span data-stu-id="eb1f2-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="eb1f2-154">상속자</span><span class="sxs-lookup"><span data-stu-id="eb1f2-154">NOTES</span></span>

## <span data-ttu-id="eb1f2-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb1f2-155">RELATED LINKS</span></span>
