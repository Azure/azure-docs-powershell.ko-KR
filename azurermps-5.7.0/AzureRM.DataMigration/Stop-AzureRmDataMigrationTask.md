---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/stop-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
ms.openlocfilehash: 7cf68cd27125580c6f0e57a7849c1fadc8cb47fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702863"
---
# <span data-ttu-id="937df-101">Stop-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="937df-101">Stop-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="937df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="937df-102">SYNOPSIS</span></span>
<span data-ttu-id="937df-103">실행 상태의 Azure 데이터베이스 마이그레이션 서비스 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="937df-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="937df-104">구문과</span><span class="sxs-lookup"><span data-stu-id="937df-104">SYNTAX</span></span>

### <span data-ttu-id="937df-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="937df-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="937df-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="937df-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="937df-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="937df-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="937df-108">설명은</span><span class="sxs-lookup"><span data-stu-id="937df-108">DESCRIPTION</span></span>
<span data-ttu-id="937df-109">Stop-AzureRmDataMigrationTask cmdlet은 실행 상태에서 데이터베이스 마이그레이션 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="937df-109">Stop-AzureRmDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="937df-110">예제의</span><span class="sxs-lookup"><span data-stu-id="937df-110">EXAMPLES</span></span>

### <span data-ttu-id="937df-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="937df-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="937df-112">위 예제에서는 project myDMSProject 및 Azure 데이터베이스 마이그레이션 서비스 인스턴스와 연결 된 myDMSTask 라는 Azure 데이터베이스 마이그레이션 서비스 작업을 중지 합니다. TestService</span><span class="sxs-lookup"><span data-stu-id="937df-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="937df-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="937df-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="937df-114">위 예제에서 Azure 데이터베이스 마이그레이션 서비스 작업이 입력 매개 변수 PSProjectTask 개체에 전달 되는 것을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="937df-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="937df-115">변수</span><span class="sxs-lookup"><span data-stu-id="937df-115">PARAMETERS</span></span>

### <span data-ttu-id="937df-116">-확인</span><span class="sxs-lookup"><span data-stu-id="937df-116">-Confirm</span></span>
<span data-ttu-id="937df-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="937df-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="937df-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="937df-118">-DefaultProfile</span></span>
<span data-ttu-id="937df-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="937df-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="937df-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="937df-120">-InputObject</span></span>
<span data-ttu-id="937df-121">PSProjectTask 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="937df-121">PSProjectTask Object.</span></span>

```yaml
Type: PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="937df-122">-이름</span><span class="sxs-lookup"><span data-stu-id="937df-122">-Name</span></span>
<span data-ttu-id="937df-123">작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="937df-123">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="937df-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="937df-124">-PassThru</span></span>
<span data-ttu-id="937df-125">True/false를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="937df-125">Returns an true/false.</span></span>
<span data-ttu-id="937df-126">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="937df-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="937df-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="937df-127">-ProjectName</span></span>
<span data-ttu-id="937df-128">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="937df-128">The name of the project.</span></span>

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

### <span data-ttu-id="937df-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="937df-129">-ResourceGroupName</span></span>
<span data-ttu-id="937df-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="937df-130">The name of the resource group .</span></span>

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

### <span data-ttu-id="937df-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="937df-131">-ResourceId</span></span>
<span data-ttu-id="937df-132">ProjectTask 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="937df-132">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="937df-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="937df-133">-ServiceName</span></span>
<span data-ttu-id="937df-134">데이터 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="937df-134">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="937df-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="937df-135">-WhatIf</span></span>
<span data-ttu-id="937df-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="937df-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="937df-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="937df-137">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="937df-138">입력</span><span class="sxs-lookup"><span data-stu-id="937df-138">INPUTS</span></span>

### <span data-ttu-id="937df-139">DataMigration. a i m.</span><span class="sxs-lookup"><span data-stu-id="937df-139">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="937df-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="937df-140">System.String</span></span>


## <span data-ttu-id="937df-141">출력</span><span class="sxs-lookup"><span data-stu-id="937df-141">OUTPUTS</span></span>

### <span data-ttu-id="937df-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="937df-142">System.Boolean</span></span>


## <span data-ttu-id="937df-143">상속자</span><span class="sxs-lookup"><span data-stu-id="937df-143">NOTES</span></span>

## <span data-ttu-id="937df-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="937df-144">RELATED LINKS</span></span>

