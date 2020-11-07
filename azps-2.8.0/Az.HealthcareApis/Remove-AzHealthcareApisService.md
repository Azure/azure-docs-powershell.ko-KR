---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/remove-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
ms.openlocfilehash: 6905e16667fd2a4378474950d928ef730ed1786e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689770"
---
# <span data-ttu-id="40175-101">Remove-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="40175-101">Remove-AzHealthcareApisService</span></span>

## <span data-ttu-id="40175-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40175-102">SYNOPSIS</span></span>
<span data-ttu-id="40175-103">서비스 인스턴스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="40175-103">Deletes a service instance.</span></span>

## <span data-ttu-id="40175-104">구문과</span><span class="sxs-lookup"><span data-stu-id="40175-104">SYNTAX</span></span>

### <span data-ttu-id="40175-105">ServiceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="40175-105">ServiceNameParameterSet (Default)</span></span>
```
Remove-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40175-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40175-106">InputObjectParameterSet</span></span>
```
Remove-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40175-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40175-107">ResourceIdParameterSet</span></span>
```
Remove-AzHealthcareApisService [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40175-108">설명은</span><span class="sxs-lookup"><span data-stu-id="40175-108">DESCRIPTION</span></span>
<span data-ttu-id="40175-109">서비스 인스턴스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="40175-109">Deletes a service instance.</span></span>

## <span data-ttu-id="40175-110">예제의</span><span class="sxs-lookup"><span data-stu-id="40175-110">EXAMPLES</span></span>

### <span data-ttu-id="40175-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="40175-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="40175-112">제공 된 리소스 그룹 내에서 제공 되는 이름으로 기존 HealthcareApis 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="40175-112">Deletes the existing HealthcareApis service with the provided name within a provided resource group.</span></span>

### <span data-ttu-id="40175-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="40175-113">Example 2</span></span>
```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService
PS C:\> Remove-AzHealthcareApisService -ResourceId $ResourceId
```

<span data-ttu-id="40175-114">제공 된 ResourceId로 기존 HealthcareApis 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="40175-114">Deletes the existing HealthcareApis service with the provided ResourceId.</span></span>

### <span data-ttu-id="40175-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="40175-115">Example 3</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName MyResourceGroup -Name MyService | Remove-AzHealthcareApisService
```

<span data-ttu-id="40175-116">제공 된 HealthcareApis service 개체를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="40175-116">Deletes the provided HealthcareApis service object.</span></span>

## <span data-ttu-id="40175-117">변수</span><span class="sxs-lookup"><span data-stu-id="40175-117">PARAMETERS</span></span>

### <span data-ttu-id="40175-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40175-118">-AsJob</span></span>
<span data-ttu-id="40175-119">백그라운드에서 cmdlet을 작업으로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="40175-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="40175-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40175-120">-DefaultProfile</span></span>
<span data-ttu-id="40175-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40175-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40175-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40175-122">-InputObject</span></span>
<span data-ttu-id="40175-123">HealthcareApis service 개체</span><span class="sxs-lookup"><span data-stu-id="40175-123">HealthcareApis service object</span></span>

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

### <span data-ttu-id="40175-124">-이름</span><span class="sxs-lookup"><span data-stu-id="40175-124">-Name</span></span>
<span data-ttu-id="40175-125">HealthcareApis 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40175-125">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="40175-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40175-126">-PassThru</span></span>
<span data-ttu-id="40175-127">제공 하는 경우 작업이 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="40175-127">If provided, returns true if the operation was successful</span></span>

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

### <span data-ttu-id="40175-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40175-128">-ResourceGroupName</span></span>
<span data-ttu-id="40175-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40175-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="40175-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40175-130">-ResourceId</span></span>
<span data-ttu-id="40175-131">HealthcareApis 서비스 ResourceId.</span><span class="sxs-lookup"><span data-stu-id="40175-131">HealthcareApis Service ResourceId.</span></span>

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

### <span data-ttu-id="40175-132">-확인</span><span class="sxs-lookup"><span data-stu-id="40175-132">-Confirm</span></span>
<span data-ttu-id="40175-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="40175-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40175-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40175-134">-WhatIf</span></span>
<span data-ttu-id="40175-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="40175-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40175-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40175-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40175-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40175-137">CommonParameters</span></span>
<span data-ttu-id="40175-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="40175-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40175-139">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="40175-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40175-140">입력</span><span class="sxs-lookup"><span data-stu-id="40175-140">INPUTS</span></span>

### <span data-ttu-id="40175-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="40175-141">System.String</span></span>

### <span data-ttu-id="40175-142">HealthcareApisService. PSHealthcareApisService/.</span><span class="sxs-lookup"><span data-stu-id="40175-142">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="40175-143">출력</span><span class="sxs-lookup"><span data-stu-id="40175-143">OUTPUTS</span></span>

### <span data-ttu-id="40175-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="40175-144">System.Boolean</span></span>

## <span data-ttu-id="40175-145">상속자</span><span class="sxs-lookup"><span data-stu-id="40175-145">NOTES</span></span>

## <span data-ttu-id="40175-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40175-146">RELATED LINKS</span></span>
