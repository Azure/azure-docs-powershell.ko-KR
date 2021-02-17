---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
ms.openlocfilehash: 7e0d8e55b5a4ab3ab22081fde94bac10f4550730
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188097"
---
# <span data-ttu-id="a01cc-101">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="a01cc-101">Get-AzSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="a01cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a01cc-102">SYNOPSIS</span></span>
<span data-ttu-id="a01cc-103">탄력적 풀 권장 사항을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a01cc-103">Gets elastic pool recommendations.</span></span>

## <span data-ttu-id="a01cc-104">구문</span><span class="sxs-lookup"><span data-stu-id="a01cc-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a01cc-105">설명</span><span class="sxs-lookup"><span data-stu-id="a01cc-105">DESCRIPTION</span></span>
<span data-ttu-id="a01cc-106">**Get-AzSqlElasticPoolRecommendation** cmdlet은 서버에 대한 탄력적 풀 권장 사항을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a01cc-106">The **Get-AzSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="a01cc-107">이러한 권장 사항에는 다음 값이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="a01cc-107">These recommendations include the following values:</span></span>
- <span data-ttu-id="a01cc-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="a01cc-108">DatabaseCollection.</span></span> <span data-ttu-id="a01cc-109">풀에 속하는 데이터베이스 이름의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="a01cc-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="a01cc-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="a01cc-110">DatabaseDtuMin.</span></span> <span data-ttu-id="a01cc-111">탄력적 풀의 데이터베이스에 대한 DTU(데이터 전송 단위)를 보장합니다.</span><span class="sxs-lookup"><span data-stu-id="a01cc-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="a01cc-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="a01cc-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="a01cc-113">탄력적 풀의 데이터베이스에 대한 DTU 한도입니다.</span><span class="sxs-lookup"><span data-stu-id="a01cc-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="a01cc-114">Dtu.</span><span class="sxs-lookup"><span data-stu-id="a01cc-114">Dtu.</span></span> <span data-ttu-id="a01cc-115">탄력적 풀에 대한 DTU 보장입니다.</span><span class="sxs-lookup"><span data-stu-id="a01cc-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="a01cc-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="a01cc-116">StorageMb.</span></span> <span data-ttu-id="a01cc-117">탄력적 풀에 대한 저장소(메가바이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="a01cc-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="a01cc-118">버전.</span><span class="sxs-lookup"><span data-stu-id="a01cc-118">Edition.</span></span> <span data-ttu-id="a01cc-119">탄력적 풀에 대한 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="a01cc-119">Edition for the elastic pool.</span></span> <span data-ttu-id="a01cc-120">이 매개 변수에 허용되는 값은 Basic, Standard 및 Premium입니다.</span><span class="sxs-lookup"><span data-stu-id="a01cc-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="a01cc-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="a01cc-121">IncludeAllDatabases.</span></span> <span data-ttu-id="a01cc-122">탄력적 풀의 모든 데이터베이스가 반환되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a01cc-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="a01cc-123">이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a01cc-123">Name.</span></span> <span data-ttu-id="a01cc-124">탄력적 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a01cc-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="a01cc-125">예제</span><span class="sxs-lookup"><span data-stu-id="a01cc-125">EXAMPLES</span></span>

### <span data-ttu-id="a01cc-126">예제 1: 서버에 대한 권장 사항 얻기</span><span class="sxs-lookup"><span data-stu-id="a01cc-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="a01cc-127">이 명령은 Server01이라는 서버에 대한 탄력적 풀 권장 사항을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a01cc-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="a01cc-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a01cc-128">PARAMETERS</span></span>

### <span data-ttu-id="a01cc-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a01cc-129">-DefaultProfile</span></span>
<span data-ttu-id="a01cc-130">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a01cc-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a01cc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a01cc-131">-ResourceGroupName</span></span>
<span data-ttu-id="a01cc-132">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a01cc-132">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a01cc-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a01cc-133">-ServerName</span></span>
<span data-ttu-id="a01cc-134">이 cmdlet이 권장 사항을 얻을 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a01cc-134">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="a01cc-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a01cc-135">-Confirm</span></span>
<span data-ttu-id="a01cc-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a01cc-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01cc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a01cc-137">-WhatIf</span></span>
<span data-ttu-id="a01cc-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a01cc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a01cc-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a01cc-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01cc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a01cc-140">CommonParameters</span></span>
<span data-ttu-id="a01cc-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a01cc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a01cc-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a01cc-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a01cc-143">입력</span><span class="sxs-lookup"><span data-stu-id="a01cc-143">INPUTS</span></span>

### <span data-ttu-id="a01cc-144">System.String</span><span class="sxs-lookup"><span data-stu-id="a01cc-144">System.String</span></span>

## <span data-ttu-id="a01cc-145">출력</span><span class="sxs-lookup"><span data-stu-id="a01cc-145">OUTPUTS</span></span>

### <span data-ttu-id="a01cc-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span><span class="sxs-lookup"><span data-stu-id="a01cc-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span></span>

## <span data-ttu-id="a01cc-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a01cc-147">NOTES</span></span>

## <span data-ttu-id="a01cc-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a01cc-148">RELATED LINKS</span></span>
