---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: 993c1968d144a5a1a56a0bd3dff46a9920a90264
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012912"
---
# <span data-ttu-id="27681-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="27681-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="27681-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27681-102">SYNOPSIS</span></span>
<span data-ttu-id="27681-103">리소스에 대한 구성을 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="27681-103">Register configuration for resource.</span></span>

## <span data-ttu-id="27681-104">구문</span><span class="sxs-lookup"><span data-stu-id="27681-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27681-105">설명</span><span class="sxs-lookup"><span data-stu-id="27681-105">DESCRIPTION</span></span>
<span data-ttu-id="27681-106">리소스에 대한 유지 관리 구성을 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="27681-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="27681-107">예제</span><span class="sxs-lookup"><span data-stu-id="27681-107">EXAMPLES</span></span>

### <span data-ttu-id="27681-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="27681-108">Example 1</span></span>
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

<span data-ttu-id="27681-109">전용 호스트에 대한 유지 관리 구성을 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="27681-109">Register maintenance configuration for dedicated host.</span></span>

## <span data-ttu-id="27681-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="27681-110">PARAMETERS</span></span>

### <span data-ttu-id="27681-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27681-111">-AsJob</span></span>
<span data-ttu-id="27681-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="27681-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27681-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="27681-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="27681-114">구성 할당 이름은 MaintenanceConfigurationName과 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="27681-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="27681-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27681-115">-DefaultProfile</span></span>
<span data-ttu-id="27681-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27681-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27681-117">-Location</span><span class="sxs-lookup"><span data-stu-id="27681-117">-Location</span></span>
<span data-ttu-id="27681-118">리소스에 대한 공백이 없는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="27681-118">The location without spaces for the resource.</span></span>

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

### <span data-ttu-id="27681-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="27681-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="27681-120">완전히 자격을 갖춘 MaintenanceConfiguration입니다.</span><span class="sxs-lookup"><span data-stu-id="27681-120">The fully qualified MaintenanceConfiguration.</span></span>

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

### <span data-ttu-id="27681-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="27681-121">-ProviderName</span></span>
<span data-ttu-id="27681-122">리소스 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27681-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="27681-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27681-123">-ResourceGroupName</span></span>
<span data-ttu-id="27681-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27681-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="27681-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27681-125">-ResourceId</span></span>
<span data-ttu-id="27681-126">구성 할당 이름은 MaintenanceConfigurationName과 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="27681-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="27681-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="27681-127">-ResourceName</span></span>
<span data-ttu-id="27681-128">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27681-128">The resource name.</span></span>

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

### <span data-ttu-id="27681-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="27681-129">-ResourceParentName</span></span>
<span data-ttu-id="27681-130">상위 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27681-130">The parent resource name.</span></span>

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

### <span data-ttu-id="27681-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="27681-131">-ResourceParentType</span></span>
<span data-ttu-id="27681-132">상위 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="27681-132">The parent resource type.</span></span>

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

### <span data-ttu-id="27681-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="27681-133">-ResourceType</span></span>
<span data-ttu-id="27681-134">리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="27681-134">The resource type.</span></span>

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

### <span data-ttu-id="27681-135">-확인</span><span class="sxs-lookup"><span data-stu-id="27681-135">-Confirm</span></span>
<span data-ttu-id="27681-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="27681-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27681-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27681-137">-WhatIf</span></span>
<span data-ttu-id="27681-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="27681-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27681-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27681-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27681-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27681-140">CommonParameters</span></span>
<span data-ttu-id="27681-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="27681-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27681-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27681-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27681-143">입력</span><span class="sxs-lookup"><span data-stu-id="27681-143">INPUTS</span></span>

### <span data-ttu-id="27681-144">System.String</span><span class="sxs-lookup"><span data-stu-id="27681-144">System.String</span></span>

## <span data-ttu-id="27681-145">출력</span><span class="sxs-lookup"><span data-stu-id="27681-145">OUTPUTS</span></span>

### <span data-ttu-id="27681-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="27681-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="27681-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="27681-147">NOTES</span></span>

## <span data-ttu-id="27681-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27681-148">RELATED LINKS</span></span>
