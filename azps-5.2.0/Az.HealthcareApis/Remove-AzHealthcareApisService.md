---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/remove-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
ms.openlocfilehash: 602ad3506f4a4fc0f8aa22128ca223e6a90f6ab5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368782"
---
# <span data-ttu-id="a3bec-101">Remove-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="a3bec-101">Remove-AzHealthcareApisService</span></span>

## <span data-ttu-id="a3bec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3bec-102">SYNOPSIS</span></span>
<span data-ttu-id="a3bec-103">서비스 인스턴스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a3bec-103">Deletes a service instance.</span></span>

## <span data-ttu-id="a3bec-104">구문</span><span class="sxs-lookup"><span data-stu-id="a3bec-104">SYNTAX</span></span>

### <span data-ttu-id="a3bec-105">ServiceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a3bec-105">ServiceNameParameterSet (Default)</span></span>
```
Remove-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3bec-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3bec-106">InputObjectParameterSet</span></span>
```
Remove-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3bec-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3bec-107">ResourceIdParameterSet</span></span>
```
Remove-AzHealthcareApisService [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3bec-108">설명</span><span class="sxs-lookup"><span data-stu-id="a3bec-108">DESCRIPTION</span></span>
<span data-ttu-id="a3bec-109">서비스 인스턴스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a3bec-109">Deletes a service instance.</span></span>

## <span data-ttu-id="a3bec-110">예제</span><span class="sxs-lookup"><span data-stu-id="a3bec-110">EXAMPLES</span></span>

### <span data-ttu-id="a3bec-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a3bec-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="a3bec-112">제공된 리소스 그룹 내에서 제공된 이름으로 기존 HealthcareApis 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a3bec-112">Deletes the existing HealthcareApis service with the provided name within a provided resource group.</span></span>

### <span data-ttu-id="a3bec-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="a3bec-113">Example 2</span></span>
```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService
PS C:\> Remove-AzHealthcareApisService -ResourceId $ResourceId
```

<span data-ttu-id="a3bec-114">제공된 ResourceId를 통해 기존 HealthcareApis 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a3bec-114">Deletes the existing HealthcareApis service with the provided ResourceId.</span></span>

### <span data-ttu-id="a3bec-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="a3bec-115">Example 3</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName MyResourceGroup -Name MyService | Remove-AzHealthcareApisService
```

<span data-ttu-id="a3bec-116">제공된 HealthcareApis 서비스 개체를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a3bec-116">Deletes the provided HealthcareApis service object.</span></span>

## <span data-ttu-id="a3bec-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3bec-117">PARAMETERS</span></span>

### <span data-ttu-id="a3bec-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3bec-118">-AsJob</span></span>
<span data-ttu-id="a3bec-119">백그라운드에서 작업으로 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a3bec-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="a3bec-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3bec-120">-DefaultProfile</span></span>
<span data-ttu-id="a3bec-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a3bec-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3bec-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3bec-122">-InputObject</span></span>
<span data-ttu-id="a3bec-123">HealthcareApis 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="a3bec-123">HealthcareApis service object</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3bec-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a3bec-124">-Name</span></span>
<span data-ttu-id="a3bec-125">HealthcareApis 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3bec-125">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3bec-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3bec-126">-PassThru</span></span>
<span data-ttu-id="a3bec-127">제공된 경우 작업이 성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a3bec-127">If provided, returns true if the operation was successful</span></span>

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

### <span data-ttu-id="a3bec-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3bec-128">-ResourceGroupName</span></span>
<span data-ttu-id="a3bec-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3bec-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3bec-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3bec-130">-ResourceId</span></span>
<span data-ttu-id="a3bec-131">HealthcareApis Service ResourceId.</span><span class="sxs-lookup"><span data-stu-id="a3bec-131">HealthcareApis Service ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3bec-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3bec-132">-Confirm</span></span>
<span data-ttu-id="a3bec-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3bec-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3bec-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3bec-134">-WhatIf</span></span>
<span data-ttu-id="a3bec-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a3bec-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3bec-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3bec-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3bec-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3bec-137">CommonParameters</span></span>
<span data-ttu-id="a3bec-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a3bec-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3bec-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a3bec-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3bec-140">입력</span><span class="sxs-lookup"><span data-stu-id="a3bec-140">INPUTS</span></span>

### <span data-ttu-id="a3bec-141">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="a3bec-141">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

### <span data-ttu-id="a3bec-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a3bec-142">System.String</span></span>

## <span data-ttu-id="a3bec-143">출력</span><span class="sxs-lookup"><span data-stu-id="a3bec-143">OUTPUTS</span></span>

### <span data-ttu-id="a3bec-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a3bec-144">System.Boolean</span></span>

## <span data-ttu-id="a3bec-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a3bec-145">NOTES</span></span>

## <span data-ttu-id="a3bec-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3bec-146">RELATED LINKS</span></span>
