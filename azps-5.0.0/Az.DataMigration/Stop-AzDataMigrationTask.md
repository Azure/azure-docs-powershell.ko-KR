---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: c7e27deb3a625d88cb2b84bfa1b53fb28ca553ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305333"
---
# <span data-ttu-id="17f94-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="17f94-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="17f94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17f94-102">SYNOPSIS</span></span>
<span data-ttu-id="17f94-103">실행 상태의 Azure 데이터베이스 마이그레이션 서비스 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="17f94-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="17f94-104">구문과</span><span class="sxs-lookup"><span data-stu-id="17f94-104">SYNTAX</span></span>

### <span data-ttu-id="17f94-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="17f94-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17f94-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17f94-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17f94-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17f94-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17f94-108">설명은</span><span class="sxs-lookup"><span data-stu-id="17f94-108">DESCRIPTION</span></span>
<span data-ttu-id="17f94-109">Stop-AzDataMigrationTask cmdlet은 실행 상태에서 데이터베이스 마이그레이션 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="17f94-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="17f94-110">예제의</span><span class="sxs-lookup"><span data-stu-id="17f94-110">EXAMPLES</span></span>

### <span data-ttu-id="17f94-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="17f94-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="17f94-112">위 예제에서는 project myDMSProject 및 Azure 데이터베이스 마이그레이션 서비스 인스턴스와 연결 된 myDMSTask 라는 Azure 데이터베이스 마이그레이션 서비스 작업을 중지 합니다. TestService</span><span class="sxs-lookup"><span data-stu-id="17f94-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="17f94-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="17f94-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="17f94-114">위 예제에서 Azure 데이터베이스 마이그레이션 서비스 작업이 입력 매개 변수 PSProjectTask 개체에 전달 되는 것을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="17f94-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="17f94-115">변수</span><span class="sxs-lookup"><span data-stu-id="17f94-115">PARAMETERS</span></span>

### <span data-ttu-id="17f94-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17f94-116">-DefaultProfile</span></span>
<span data-ttu-id="17f94-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="17f94-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17f94-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17f94-118">-InputObject</span></span>
<span data-ttu-id="17f94-119">PSProjectTask 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="17f94-119">PSProjectTask Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17f94-120">-이름</span><span class="sxs-lookup"><span data-stu-id="17f94-120">-Name</span></span>
<span data-ttu-id="17f94-121">작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17f94-121">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17f94-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17f94-122">-PassThru</span></span>
<span data-ttu-id="17f94-123">True/false를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="17f94-123">Returns an true/false.</span></span>
<span data-ttu-id="17f94-124">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17f94-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="17f94-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="17f94-125">-ProjectName</span></span>
<span data-ttu-id="17f94-126">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17f94-126">The name of the project.</span></span>

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

### <span data-ttu-id="17f94-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17f94-127">-ResourceGroupName</span></span>
<span data-ttu-id="17f94-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17f94-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="17f94-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17f94-129">-ResourceId</span></span>
<span data-ttu-id="17f94-130">ProjectTask 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="17f94-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="17f94-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="17f94-131">-ServiceName</span></span>
<span data-ttu-id="17f94-132">데이터베이스 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17f94-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="17f94-133">-확인</span><span class="sxs-lookup"><span data-stu-id="17f94-133">-Confirm</span></span>
<span data-ttu-id="17f94-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="17f94-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17f94-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17f94-135">-WhatIf</span></span>
<span data-ttu-id="17f94-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="17f94-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17f94-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17f94-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17f94-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17f94-138">CommonParameters</span></span>
<span data-ttu-id="17f94-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17f94-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17f94-140">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17f94-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17f94-141">입력</span><span class="sxs-lookup"><span data-stu-id="17f94-141">INPUTS</span></span>

### <span data-ttu-id="17f94-142">DataMigration. a i m.</span><span class="sxs-lookup"><span data-stu-id="17f94-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="17f94-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="17f94-143">System.String</span></span>

## <span data-ttu-id="17f94-144">출력</span><span class="sxs-lookup"><span data-stu-id="17f94-144">OUTPUTS</span></span>

### <span data-ttu-id="17f94-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="17f94-145">System.Boolean</span></span>

## <span data-ttu-id="17f94-146">상속자</span><span class="sxs-lookup"><span data-stu-id="17f94-146">NOTES</span></span>

## <span data-ttu-id="17f94-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17f94-147">RELATED LINKS</span></span>
