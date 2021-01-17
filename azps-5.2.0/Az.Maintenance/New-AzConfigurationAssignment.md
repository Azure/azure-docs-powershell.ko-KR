---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: 9754c3efc87d0e607c613789e6e27320f430aa06
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340826"
---
# <span data-ttu-id="23c7e-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="23c7e-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="23c7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="23c7e-103">리소스에 대한 구성을 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="23c7e-103">Register configuration for resource.</span></span>

## <span data-ttu-id="23c7e-104">구문</span><span class="sxs-lookup"><span data-stu-id="23c7e-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="23c7e-105">설명</span><span class="sxs-lookup"><span data-stu-id="23c7e-105">DESCRIPTION</span></span>
<span data-ttu-id="23c7e-106">리소스에 대한 유지 관리 구성을 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="23c7e-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="23c7e-107">예제</span><span class="sxs-lookup"><span data-stu-id="23c7e-107">EXAMPLES</span></span>

### <span data-ttu-id="23c7e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="23c7e-108">Example 1</span></span>
```powershell
PS C:\> New-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName -MaintenanceConfigurationId $maintenanceConfigurationCreated.Id -Location $location


Location                   : westus2
MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
ResourceId                 : 7b32ed22-dc7b-4a17-9c42-36c024f4c9f9
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="23c7e-109">전용 호스트에 대한 유지 관리 구성을 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="23c7e-109">Register maintenance configuration for dedicated host.</span></span>

## <span data-ttu-id="23c7e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23c7e-110">PARAMETERS</span></span>

### <span data-ttu-id="23c7e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23c7e-111">-AsJob</span></span>
<span data-ttu-id="23c7e-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="23c7e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23c7e-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="23c7e-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="23c7e-114">구성 할당 이름은 MaintenanceConfigurationName과 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="23c7e-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23c7e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23c7e-115">-DefaultProfile</span></span>
<span data-ttu-id="23c7e-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23c7e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23c7e-117">-Location</span><span class="sxs-lookup"><span data-stu-id="23c7e-117">-Location</span></span>
<span data-ttu-id="23c7e-118">리소스에 대한 공백이 없는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="23c7e-118">The location without spaces for the resource.</span></span>

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

### <span data-ttu-id="23c7e-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="23c7e-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="23c7e-120">정식 MaintenanceConfiguration입니다.</span><span class="sxs-lookup"><span data-stu-id="23c7e-120">The fully qualified MaintenanceConfiguration.</span></span>

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

### <span data-ttu-id="23c7e-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="23c7e-121">-ProviderName</span></span>
<span data-ttu-id="23c7e-122">리소스 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23c7e-122">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23c7e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23c7e-123">-ResourceGroupName</span></span>
<span data-ttu-id="23c7e-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23c7e-124">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23c7e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23c7e-125">-ResourceId</span></span>
<span data-ttu-id="23c7e-126">구성 할당 이름은 MaintenanceConfigurationName과 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="23c7e-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="23c7e-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="23c7e-127">-ResourceName</span></span>
<span data-ttu-id="23c7e-128">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23c7e-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23c7e-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="23c7e-129">-ResourceParentName</span></span>
<span data-ttu-id="23c7e-130">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23c7e-130">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23c7e-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="23c7e-131">-ResourceParentType</span></span>
<span data-ttu-id="23c7e-132">부모 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="23c7e-132">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23c7e-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="23c7e-133">-ResourceType</span></span>
<span data-ttu-id="23c7e-134">리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="23c7e-134">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23c7e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23c7e-135">-Confirm</span></span>
<span data-ttu-id="23c7e-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="23c7e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23c7e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23c7e-137">-WhatIf</span></span>
<span data-ttu-id="23c7e-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="23c7e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23c7e-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23c7e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23c7e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23c7e-140">CommonParameters</span></span>
<span data-ttu-id="23c7e-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="23c7e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23c7e-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="23c7e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23c7e-143">입력</span><span class="sxs-lookup"><span data-stu-id="23c7e-143">INPUTS</span></span>

### <span data-ttu-id="23c7e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="23c7e-144">System.String</span></span>

## <span data-ttu-id="23c7e-145">출력</span><span class="sxs-lookup"><span data-stu-id="23c7e-145">OUTPUTS</span></span>

### <span data-ttu-id="23c7e-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="23c7e-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="23c7e-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="23c7e-147">NOTES</span></span>

## <span data-ttu-id="23c7e-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23c7e-148">RELATED LINKS</span></span>
