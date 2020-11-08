---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
ms.openlocfilehash: 3362fd6b1e60fa975277c97ea76a8e8c15ee29a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217734"
---
# <span data-ttu-id="434ce-101">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="434ce-101">Remove-AzIotHubModule</span></span>

## <span data-ttu-id="434ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="434ce-102">SYNOPSIS</span></span>
<span data-ttu-id="434ce-103">IoT Hub의 대상 IoT 장치에서 모듈을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="434ce-103">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="434ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="434ce-104">SYNTAX</span></span>

### <span data-ttu-id="434ce-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="434ce-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="434ce-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="434ce-106">InputObjectSet</span></span>
```
Remove-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="434ce-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="434ce-107">ResourceIdSet</span></span>
```
Remove-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="434ce-108">설명은</span><span class="sxs-lookup"><span data-stu-id="434ce-108">DESCRIPTION</span></span>
<span data-ttu-id="434ce-109">IoT Hub의 대상 IoT 장치에서 모듈을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="434ce-109">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="434ce-110">예제의</span><span class="sxs-lookup"><span data-stu-id="434ce-110">EXAMPLES</span></span>

### <span data-ttu-id="434ce-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="434ce-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -PassThru

True
```

<span data-ttu-id="434ce-112">Iot 장치 모듈을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="434ce-112">Delete an Iot device module.</span></span>

### <span data-ttu-id="434ce-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="434ce-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="434ce-114">모든 Iot 장치 모듈을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="434ce-114">Delete all Iot device modules.</span></span>

## <span data-ttu-id="434ce-115">변수</span><span class="sxs-lookup"><span data-stu-id="434ce-115">PARAMETERS</span></span>

### <span data-ttu-id="434ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="434ce-116">-DefaultProfile</span></span>
<span data-ttu-id="434ce-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="434ce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="434ce-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="434ce-118">-DeviceId</span></span>
<span data-ttu-id="434ce-119">대상 장치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="434ce-119">Target Device Id.</span></span>

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

### <span data-ttu-id="434ce-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="434ce-120">-InputObject</span></span>
<span data-ttu-id="434ce-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="434ce-121">IotHub object</span></span>

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

### <span data-ttu-id="434ce-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="434ce-122">-IotHubName</span></span>
<span data-ttu-id="434ce-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="434ce-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="434ce-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="434ce-124">-ModuleId</span></span>
<span data-ttu-id="434ce-125">대상 모듈 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="434ce-125">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="434ce-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="434ce-126">-PassThru</span></span>
<span data-ttu-id="434ce-127">Boolean 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="434ce-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="434ce-128">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="434ce-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="434ce-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="434ce-129">-ResourceGroupName</span></span>
<span data-ttu-id="434ce-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="434ce-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="434ce-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="434ce-131">-ResourceId</span></span>
<span data-ttu-id="434ce-132">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="434ce-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="434ce-133">-확인</span><span class="sxs-lookup"><span data-stu-id="434ce-133">-Confirm</span></span>
<span data-ttu-id="434ce-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="434ce-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="434ce-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="434ce-135">-WhatIf</span></span>
<span data-ttu-id="434ce-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="434ce-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="434ce-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="434ce-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="434ce-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="434ce-138">CommonParameters</span></span>
<span data-ttu-id="434ce-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="434ce-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="434ce-140">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="434ce-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="434ce-141">입력</span><span class="sxs-lookup"><span data-stu-id="434ce-141">INPUTS</span></span>

### <span data-ttu-id="434ce-142">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="434ce-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="434ce-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="434ce-143">System.String</span></span>

## <span data-ttu-id="434ce-144">출력</span><span class="sxs-lookup"><span data-stu-id="434ce-144">OUTPUTS</span></span>

### <span data-ttu-id="434ce-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="434ce-145">System.Boolean</span></span>

## <span data-ttu-id="434ce-146">상속자</span><span class="sxs-lookup"><span data-stu-id="434ce-146">NOTES</span></span>

## <span data-ttu-id="434ce-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="434ce-147">RELATED LINKS</span></span>
