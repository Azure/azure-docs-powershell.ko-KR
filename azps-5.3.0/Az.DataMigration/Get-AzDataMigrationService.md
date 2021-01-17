---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
ms.openlocfilehash: 287e4db59ae19efec604da9b63958b5ea74b747f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489032"
---
# <span data-ttu-id="e09c7-101">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e09c7-101">Get-AzDataMigrationService</span></span>

## <span data-ttu-id="e09c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e09c7-102">SYNOPSIS</span></span>
<span data-ttu-id="e09c7-103">Azure Database Migration Service의 인스턴스와 연결된 속성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="e09c7-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

## <span data-ttu-id="e09c7-104">구문</span><span class="sxs-lookup"><span data-stu-id="e09c7-104">SYNTAX</span></span>

### <span data-ttu-id="e09c7-105">ResourceGroupSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e09c7-105">ResourceGroupSet (Default)</span></span>
```
Get-AzDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e09c7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e09c7-106">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e09c7-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="e09c7-107">ServiceNameGroupSet</span></span>
```
Get-AzDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e09c7-108">설명</span><span class="sxs-lookup"><span data-stu-id="e09c7-108">DESCRIPTION</span></span>
<span data-ttu-id="e09c7-109">이 Get-AzDataMigrationService cmdlet은 입력 매개 변수로 서비스 이름 및 Azure 리소스 그룹 이름을 기반으로 Azure Database Migration Service의 인스턴스와 연결된 속성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="e09c7-109">The Get-AzDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="e09c7-110">예제</span><span class="sxs-lookup"><span data-stu-id="e09c7-110">EXAMPLES</span></span>

### <span data-ttu-id="e09c7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e09c7-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="e09c7-112">위의 예제에서는 testService라는 Azure Database Migration Service 인스턴스의 속성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="e09c7-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="e09c7-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e09c7-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="e09c7-114">위의 예제에서는 testResourceGroup이라는 리소스 그룹에서 Azure Database Migration Services를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="e09c7-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="e09c7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e09c7-115">PARAMETERS</span></span>

### <span data-ttu-id="e09c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e09c7-116">-DefaultProfile</span></span>
<span data-ttu-id="e09c7-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e09c7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e09c7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e09c7-118">-Name</span></span>
<span data-ttu-id="e09c7-119">Database Migration Service의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e09c7-119">Name of Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e09c7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e09c7-120">-ResourceGroupName</span></span>
<span data-ttu-id="e09c7-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e09c7-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e09c7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e09c7-122">-ResourceId</span></span>
<span data-ttu-id="e09c7-123">DataMigrationService 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e09c7-123">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="e09c7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e09c7-124">CommonParameters</span></span>
<span data-ttu-id="e09c7-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e09c7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e09c7-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e09c7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e09c7-127">입력</span><span class="sxs-lookup"><span data-stu-id="e09c7-127">INPUTS</span></span>

### <span data-ttu-id="e09c7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e09c7-128">System.String</span></span>

## <span data-ttu-id="e09c7-129">출력</span><span class="sxs-lookup"><span data-stu-id="e09c7-129">OUTPUTS</span></span>

### <span data-ttu-id="e09c7-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e09c7-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="e09c7-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e09c7-131">NOTES</span></span>

## <span data-ttu-id="e09c7-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e09c7-132">RELATED LINKS</span></span>
