---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
ms.openlocfilehash: f5463015b93c209c6cf8952c566e9656da2fba18
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048239"
---
# <span data-ttu-id="04813-101">Remove-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="04813-101">Remove-AzIotHubDeployment</span></span>

## <span data-ttu-id="04813-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04813-102">SYNOPSIS</span></span>
<span data-ttu-id="04813-103">IoT Edge 배포를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="04813-103">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="04813-104">구문과</span><span class="sxs-lookup"><span data-stu-id="04813-104">SYNTAX</span></span>

### <span data-ttu-id="04813-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="04813-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04813-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="04813-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04813-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="04813-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04813-108">설명은</span><span class="sxs-lookup"><span data-stu-id="04813-108">DESCRIPTION</span></span>
<span data-ttu-id="04813-109"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring자세한 내용은을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="04813-109">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="04813-110">예제의</span><span class="sxs-lookup"><span data-stu-id="04813-110">EXAMPLES</span></span>

### <span data-ttu-id="04813-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="04813-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="04813-112">IoT Edge 배포를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="04813-112">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="04813-113">변수</span><span class="sxs-lookup"><span data-stu-id="04813-113">PARAMETERS</span></span>

### <span data-ttu-id="04813-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04813-114">-DefaultProfile</span></span>
<span data-ttu-id="04813-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04813-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04813-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04813-116">-InputObject</span></span>
<span data-ttu-id="04813-117">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="04813-117">IotHub object</span></span>

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

### <span data-ttu-id="04813-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="04813-118">-IotHubName</span></span>
<span data-ttu-id="04813-119">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="04813-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="04813-120">-이름</span><span class="sxs-lookup"><span data-stu-id="04813-120">-Name</span></span>
<span data-ttu-id="04813-121">배포의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="04813-121">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="04813-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04813-122">-PassThru</span></span>
<span data-ttu-id="04813-123">Boolean 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04813-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="04813-124">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04813-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="04813-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04813-125">-ResourceGroupName</span></span>
<span data-ttu-id="04813-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04813-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="04813-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04813-127">-ResourceId</span></span>
<span data-ttu-id="04813-128">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="04813-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="04813-129">-확인</span><span class="sxs-lookup"><span data-stu-id="04813-129">-Confirm</span></span>
<span data-ttu-id="04813-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="04813-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04813-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04813-131">-WhatIf</span></span>
<span data-ttu-id="04813-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="04813-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04813-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04813-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04813-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04813-134">CommonParameters</span></span>
<span data-ttu-id="04813-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="04813-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04813-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04813-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04813-137">입력</span><span class="sxs-lookup"><span data-stu-id="04813-137">INPUTS</span></span>

### <span data-ttu-id="04813-138">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="04813-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="04813-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="04813-139">System.String</span></span>

## <span data-ttu-id="04813-140">출력</span><span class="sxs-lookup"><span data-stu-id="04813-140">OUTPUTS</span></span>

### <span data-ttu-id="04813-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="04813-141">System.Boolean</span></span>

## <span data-ttu-id="04813-142">상속자</span><span class="sxs-lookup"><span data-stu-id="04813-142">NOTES</span></span>

## <span data-ttu-id="04813-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04813-143">RELATED LINKS</span></span>
