---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
ms.openlocfilehash: 3d137f93c32b77afd29a833086ff5c55823bc104
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043799"
---
# <span data-ttu-id="9de81-101">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="9de81-101">Remove-AzIotHubDevice</span></span>

## <span data-ttu-id="9de81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9de81-102">SYNOPSIS</span></span>
<span data-ttu-id="9de81-103">IoT Hub 장치를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de81-103">Delete an IoT Hub device.</span></span>

## <span data-ttu-id="9de81-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9de81-104">SYNTAX</span></span>

### <span data-ttu-id="9de81-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9de81-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9de81-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9de81-106">InputObjectSet</span></span>
```
Remove-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9de81-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9de81-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9de81-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9de81-108">DESCRIPTION</span></span>
<span data-ttu-id="9de81-109">Iot Hub의 모든 장치 또는 특정 장치를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de81-109">Delete all devices or a specific device from an Iot Hub.</span></span>

## <span data-ttu-id="9de81-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9de81-110">EXAMPLES</span></span>

### <span data-ttu-id="9de81-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9de81-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="9de81-112">모든 Iot Hub 장치를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de81-112">Delete all Iot Hub devices.</span></span>

### <span data-ttu-id="9de81-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="9de81-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="9de81-114">Iot Hub 장치를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de81-114">Delete an Iot Hub device.</span></span>

## <span data-ttu-id="9de81-115">변수</span><span class="sxs-lookup"><span data-stu-id="9de81-115">PARAMETERS</span></span>

### <span data-ttu-id="9de81-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9de81-116">-DefaultProfile</span></span>
<span data-ttu-id="9de81-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9de81-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9de81-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="9de81-118">-DeviceId</span></span>
<span data-ttu-id="9de81-119">대상 장치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="9de81-119">Target Device Id.</span></span>

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

### <span data-ttu-id="9de81-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9de81-120">-InputObject</span></span>
<span data-ttu-id="9de81-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="9de81-121">IotHub object</span></span>

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

### <span data-ttu-id="9de81-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="9de81-122">-IotHubName</span></span>
<span data-ttu-id="9de81-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="9de81-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9de81-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9de81-124">-PassThru</span></span>
<span data-ttu-id="9de81-125">Boolean 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9de81-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="9de81-126">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9de81-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9de81-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9de81-127">-ResourceGroupName</span></span>
<span data-ttu-id="9de81-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9de81-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9de81-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9de81-129">-ResourceId</span></span>
<span data-ttu-id="9de81-130">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="9de81-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9de81-131">-확인</span><span class="sxs-lookup"><span data-stu-id="9de81-131">-Confirm</span></span>
<span data-ttu-id="9de81-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de81-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9de81-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9de81-133">-WhatIf</span></span>
<span data-ttu-id="9de81-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9de81-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9de81-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9de81-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9de81-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de81-136">CommonParameters</span></span>
<span data-ttu-id="9de81-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de81-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de81-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9de81-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de81-139">입력</span><span class="sxs-lookup"><span data-stu-id="9de81-139">INPUTS</span></span>

### <span data-ttu-id="9de81-140">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="9de81-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9de81-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9de81-141">System.String</span></span>

## <span data-ttu-id="9de81-142">출력</span><span class="sxs-lookup"><span data-stu-id="9de81-142">OUTPUTS</span></span>

### <span data-ttu-id="9de81-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9de81-143">System.Boolean</span></span>

## <span data-ttu-id="9de81-144">상속자</span><span class="sxs-lookup"><span data-stu-id="9de81-144">NOTES</span></span>

## <span data-ttu-id="9de81-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9de81-145">RELATED LINKS</span></span>
