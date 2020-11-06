---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
ms.openlocfilehash: 8ec046df13302ece90e57bcb722816f2019ff2e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535999"
---
# <span data-ttu-id="458eb-101">Remove-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="458eb-101">Remove-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="458eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="458eb-102">SYNOPSIS</span></span>
<span data-ttu-id="458eb-103">Azure에서 Azure 데이터베이스 마이그레이션 서비스 프로젝트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="458eb-103">Removes an Azure Database Migration Service project from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="458eb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="458eb-104">SYNTAX</span></span>

### <span data-ttu-id="458eb-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="458eb-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="458eb-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="458eb-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="458eb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="458eb-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="458eb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="458eb-108">DESCRIPTION</span></span>
<span data-ttu-id="458eb-109">Remove-AzureRmDataMigrationProject cmdlet은 azure에서 Azure 데이터베이스 마이그레이션 서비스 프로젝트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="458eb-109">The Remove-AzureRmDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="458eb-110">DeleteRunningTask 매개 변수를 제공 하면 제거 되는 프로젝트와 관련 된 모든 Azure 데이터베이스 마이그레이션 서비스 작업이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="458eb-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="458eb-111">예제의</span><span class="sxs-lookup"><span data-stu-id="458eb-111">EXAMPLES</span></span>

### <span data-ttu-id="458eb-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="458eb-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="458eb-113">위 예제에서는 이름을 입력 매개 변수로 사용 하 여 Azure에서 myDMProject 라는 Azure 데이터베이스 마이그레이션 서비스 프로젝트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="458eb-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="458eb-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="458eb-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="458eb-115">위 예제에서는 PSProject 개체를 기반으로 하는 Azure 데이터베이스 마이그레이션 서비스 프로젝트를 입력 매개 변수로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="458eb-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="458eb-116">변수</span><span class="sxs-lookup"><span data-stu-id="458eb-116">PARAMETERS</span></span>

### <span data-ttu-id="458eb-117">-확인</span><span class="sxs-lookup"><span data-stu-id="458eb-117">-Confirm</span></span>
<span data-ttu-id="458eb-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="458eb-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="458eb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="458eb-119">-DefaultProfile</span></span>
<span data-ttu-id="458eb-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="458eb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="458eb-121">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="458eb-121">-DeleteRunningTask</span></span>
<span data-ttu-id="458eb-122">실행 중인 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="458eb-122">Delete any running task</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="458eb-123">-Force</span><span class="sxs-lookup"><span data-stu-id="458eb-123">-Force</span></span>
<span data-ttu-id="458eb-124">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="458eb-124">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="458eb-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="458eb-125">-InputObject</span></span>
<span data-ttu-id="458eb-126">PSProject 개체.</span><span class="sxs-lookup"><span data-stu-id="458eb-126">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="458eb-127">-이름</span><span class="sxs-lookup"><span data-stu-id="458eb-127">-Name</span></span>
<span data-ttu-id="458eb-128">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="458eb-128">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="458eb-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="458eb-129">-PassThru</span></span>
<span data-ttu-id="458eb-130">True/false를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="458eb-130">Returns an true/false.</span></span>
<span data-ttu-id="458eb-131">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="458eb-131">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="458eb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="458eb-132">-ResourceGroupName</span></span>
<span data-ttu-id="458eb-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="458eb-133">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="458eb-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="458eb-134">-ResourceId</span></span>
<span data-ttu-id="458eb-135">프로젝트 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="458eb-135">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="458eb-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="458eb-136">-ServiceName</span></span>
<span data-ttu-id="458eb-137">데이터 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="458eb-137">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="458eb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="458eb-138">-WhatIf</span></span>
<span data-ttu-id="458eb-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="458eb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="458eb-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="458eb-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="458eb-141">입력</span><span class="sxs-lookup"><span data-stu-id="458eb-141">INPUTS</span></span>

### <span data-ttu-id="458eb-142">DataMigration. a i m. PSProject</span><span class="sxs-lookup"><span data-stu-id="458eb-142">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="458eb-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="458eb-143">System.String</span></span>


## <span data-ttu-id="458eb-144">출력</span><span class="sxs-lookup"><span data-stu-id="458eb-144">OUTPUTS</span></span>

### <span data-ttu-id="458eb-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="458eb-145">System.Boolean</span></span>


## <span data-ttu-id="458eb-146">상속자</span><span class="sxs-lookup"><span data-stu-id="458eb-146">NOTES</span></span>

## <span data-ttu-id="458eb-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="458eb-147">RELATED LINKS</span></span>

