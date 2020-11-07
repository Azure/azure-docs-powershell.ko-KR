---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
ms.openlocfilehash: 53dc4841dbbdcb7f3d855630b69a94320b4dfeff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701024"
---
# <span data-ttu-id="3de8b-101">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="3de8b-101">Remove-AzDataMigrationProject</span></span>

## <span data-ttu-id="3de8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3de8b-102">SYNOPSIS</span></span>
<span data-ttu-id="3de8b-103">Azure에서 Azure 데이터베이스 마이그레이션 서비스 프로젝트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3de8b-103">Removes an Azure Database Migration Service project from Azure.</span></span>

## <span data-ttu-id="3de8b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3de8b-104">SYNTAX</span></span>

### <span data-ttu-id="3de8b-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3de8b-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3de8b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3de8b-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3de8b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3de8b-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3de8b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3de8b-108">DESCRIPTION</span></span>
<span data-ttu-id="3de8b-109">Remove-AzDataMigrationProject cmdlet은 azure에서 Azure 데이터베이스 마이그레이션 서비스 프로젝트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3de8b-109">The Remove-AzDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="3de8b-110">DeleteRunningTask 매개 변수를 제공 하면 제거 되는 프로젝트와 관련 된 모든 Azure 데이터베이스 마이그레이션 서비스 작업이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3de8b-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="3de8b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="3de8b-111">EXAMPLES</span></span>

### <span data-ttu-id="3de8b-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="3de8b-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="3de8b-113">위 예제에서는 이름을 입력 매개 변수로 사용 하 여 Azure에서 myDMProject 라는 Azure 데이터베이스 마이그레이션 서비스 프로젝트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3de8b-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="3de8b-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="3de8b-114">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="3de8b-115">위 예제에서는 PSProject 개체를 기반으로 하는 Azure 데이터베이스 마이그레이션 서비스 프로젝트를 입력 매개 변수로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3de8b-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="3de8b-116">변수</span><span class="sxs-lookup"><span data-stu-id="3de8b-116">PARAMETERS</span></span>

### <span data-ttu-id="3de8b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3de8b-117">-DefaultProfile</span></span>
<span data-ttu-id="3de8b-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3de8b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3de8b-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="3de8b-119">-DeleteRunningTask</span></span>
<span data-ttu-id="3de8b-120">실행 중인 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="3de8b-120">Delete any running task</span></span>

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

### <span data-ttu-id="3de8b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3de8b-121">-Force</span></span>
<span data-ttu-id="3de8b-122">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="3de8b-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="3de8b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3de8b-123">-InputObject</span></span>
<span data-ttu-id="3de8b-124">PSProject 개체.</span><span class="sxs-lookup"><span data-stu-id="3de8b-124">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3de8b-125">-이름</span><span class="sxs-lookup"><span data-stu-id="3de8b-125">-Name</span></span>
<span data-ttu-id="3de8b-126">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3de8b-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de8b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3de8b-127">-PassThru</span></span>
<span data-ttu-id="3de8b-128">True/false를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3de8b-128">Returns an true/false.</span></span>
<span data-ttu-id="3de8b-129">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3de8b-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3de8b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3de8b-130">-ResourceGroupName</span></span>
<span data-ttu-id="3de8b-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3de8b-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de8b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3de8b-132">-ResourceId</span></span>
<span data-ttu-id="3de8b-133">프로젝트 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="3de8b-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="3de8b-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3de8b-134">-ServiceName</span></span>
<span data-ttu-id="3de8b-135">데이터베이스 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3de8b-135">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de8b-136">-확인</span><span class="sxs-lookup"><span data-stu-id="3de8b-136">-Confirm</span></span>
<span data-ttu-id="3de8b-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3de8b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3de8b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3de8b-138">-WhatIf</span></span>
<span data-ttu-id="3de8b-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3de8b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3de8b-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3de8b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3de8b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3de8b-141">CommonParameters</span></span>
<span data-ttu-id="3de8b-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3de8b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3de8b-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3de8b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3de8b-144">입력</span><span class="sxs-lookup"><span data-stu-id="3de8b-144">INPUTS</span></span>

### <span data-ttu-id="3de8b-145">DataMigration. a i m. PSProject</span><span class="sxs-lookup"><span data-stu-id="3de8b-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="3de8b-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3de8b-146">System.String</span></span>

## <span data-ttu-id="3de8b-147">출력</span><span class="sxs-lookup"><span data-stu-id="3de8b-147">OUTPUTS</span></span>

### <span data-ttu-id="3de8b-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="3de8b-148">System.Boolean</span></span>

## <span data-ttu-id="3de8b-149">상속자</span><span class="sxs-lookup"><span data-stu-id="3de8b-149">NOTES</span></span>

## <span data-ttu-id="3de8b-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3de8b-150">RELATED LINKS</span></span>
