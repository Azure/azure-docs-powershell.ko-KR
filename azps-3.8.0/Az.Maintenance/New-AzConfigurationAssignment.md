---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: f0c5c52773d5750b86ce82d696e9130df76f4700
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044222"
---
# <span data-ttu-id="0050e-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="0050e-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="0050e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0050e-102">SYNOPSIS</span></span>
<span data-ttu-id="0050e-103">리소스에 대 한 구성을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0050e-103">Register configuration for resource.</span></span>

## <span data-ttu-id="0050e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0050e-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0050e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0050e-105">DESCRIPTION</span></span>
<span data-ttu-id="0050e-106">리소스에 대 한 유지 관리 구성을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0050e-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="0050e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0050e-107">EXAMPLES</span></span>

### <span data-ttu-id="0050e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0050e-108">Example 1</span></span>
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

<span data-ttu-id="0050e-109">Didicated host에 대 한 유지 관리 구성을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0050e-109">Register maintenance configuration for didicated host.</span></span>

## <span data-ttu-id="0050e-110">변수</span><span class="sxs-lookup"><span data-stu-id="0050e-110">PARAMETERS</span></span>

### <span data-ttu-id="0050e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0050e-111">-AsJob</span></span>
<span data-ttu-id="0050e-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0050e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0050e-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="0050e-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="0050e-114">구성 할당 이름은 MaintenanceConfigurationName와 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0050e-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="0050e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0050e-115">-DefaultProfile</span></span>
<span data-ttu-id="0050e-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0050e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0050e-117">-위치</span><span class="sxs-lookup"><span data-stu-id="0050e-117">-Location</span></span>
<span data-ttu-id="0050e-118">리소스에 대 한 공간이 없는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0050e-118">The location without spaces for the resource.</span></span>

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

### <span data-ttu-id="0050e-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0050e-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="0050e-120">정규화 된 MaintenanceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0050e-120">The fully qualified MaintenanceConfiguration.</span></span>

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

### <span data-ttu-id="0050e-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="0050e-121">-ProviderName</span></span>
<span data-ttu-id="0050e-122">리소스 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0050e-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="0050e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0050e-123">-ResourceGroupName</span></span>
<span data-ttu-id="0050e-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0050e-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="0050e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0050e-125">-ResourceId</span></span>
<span data-ttu-id="0050e-126">구성 할당 이름은 MaintenanceConfigurationName와 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0050e-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="0050e-127">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="0050e-127">-ResourceName</span></span>
<span data-ttu-id="0050e-128">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0050e-128">The resource name.</span></span>

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

### <span data-ttu-id="0050e-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="0050e-129">-ResourceParentName</span></span>
<span data-ttu-id="0050e-130">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0050e-130">The parent resource name.</span></span>

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

### <span data-ttu-id="0050e-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="0050e-131">-ResourceParentType</span></span>
<span data-ttu-id="0050e-132">부모 리소스 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="0050e-132">The parent resource type.</span></span>

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

### <span data-ttu-id="0050e-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0050e-133">-ResourceType</span></span>
<span data-ttu-id="0050e-134">리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="0050e-134">The resource type.</span></span>

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

### <span data-ttu-id="0050e-135">-확인</span><span class="sxs-lookup"><span data-stu-id="0050e-135">-Confirm</span></span>
<span data-ttu-id="0050e-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0050e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0050e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0050e-137">-WhatIf</span></span>
<span data-ttu-id="0050e-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0050e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0050e-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0050e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0050e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0050e-140">CommonParameters</span></span>
<span data-ttu-id="0050e-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0050e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0050e-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0050e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0050e-143">입력</span><span class="sxs-lookup"><span data-stu-id="0050e-143">INPUTS</span></span>

### <span data-ttu-id="0050e-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0050e-144">System.String</span></span>

## <span data-ttu-id="0050e-145">출력</span><span class="sxs-lookup"><span data-stu-id="0050e-145">OUTPUTS</span></span>

### <span data-ttu-id="0050e-146">Microsoft. Azure. PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="0050e-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="0050e-147">상속자</span><span class="sxs-lookup"><span data-stu-id="0050e-147">NOTES</span></span>

## <span data-ttu-id="0050e-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0050e-148">RELATED LINKS</span></span>
