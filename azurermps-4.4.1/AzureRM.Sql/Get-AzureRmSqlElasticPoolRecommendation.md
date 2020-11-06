---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
ms.openlocfilehash: 47d56a0c15cc3ecf9656ae6c14600adf6a1e2cf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529080"
---
# <span data-ttu-id="038ee-101">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="038ee-101">Get-AzureRmSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="038ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="038ee-102">SYNOPSIS</span></span>
<span data-ttu-id="038ee-103">탄력적 풀 추천 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="038ee-103">Gets elastic pool recommendations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="038ee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="038ee-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="038ee-105">설명은</span><span class="sxs-lookup"><span data-stu-id="038ee-105">DESCRIPTION</span></span>
<span data-ttu-id="038ee-106">**AzureRmSqlElasticPoolRecommendation** cmdlet은 서버에 대 한 탄력적 풀 추천 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="038ee-106">The **Get-AzureRmSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="038ee-107">이러한 권장 사항에는 다음 값이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="038ee-107">These recommendations include the following values:</span></span>

- <span data-ttu-id="038ee-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="038ee-108">DatabaseCollection.</span></span> <span data-ttu-id="038ee-109">풀에 속한 데이터베이스 이름의 모음입니다.</span><span class="sxs-lookup"><span data-stu-id="038ee-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="038ee-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="038ee-110">DatabaseDtuMin.</span></span> <span data-ttu-id="038ee-111">탄력적 풀의 데이터베이스에 대 한 DTU (데이터 전송 단위) 보장.</span><span class="sxs-lookup"><span data-stu-id="038ee-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="038ee-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="038ee-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="038ee-113">탄력적 풀의 데이터베이스에 대 한 DTU 캡입니다.</span><span class="sxs-lookup"><span data-stu-id="038ee-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="038ee-114">Dtu.</span><span class="sxs-lookup"><span data-stu-id="038ee-114">Dtu.</span></span> <span data-ttu-id="038ee-115">탄력적 풀에 대 한 DTU 보증입니다.</span><span class="sxs-lookup"><span data-stu-id="038ee-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="038ee-116">StorageMb</span><span class="sxs-lookup"><span data-stu-id="038ee-116">StorageMb.</span></span> <span data-ttu-id="038ee-117">탄력적 풀의 저장소 (mb)입니다.</span><span class="sxs-lookup"><span data-stu-id="038ee-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="038ee-118">평가판.</span><span class="sxs-lookup"><span data-stu-id="038ee-118">Edition.</span></span> <span data-ttu-id="038ee-119">탄력적 풀 용 에디션.</span><span class="sxs-lookup"><span data-stu-id="038ee-119">Edition for the elastic pool.</span></span> <span data-ttu-id="038ee-120">이 매개 변수에 허용 되는 값은 Basic, Standard 및 Premium입니다.</span><span class="sxs-lookup"><span data-stu-id="038ee-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="038ee-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="038ee-121">IncludeAllDatabases.</span></span> <span data-ttu-id="038ee-122">탄력적 풀의 모든 데이터베이스가 반환 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="038ee-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="038ee-123">성을.</span><span class="sxs-lookup"><span data-stu-id="038ee-123">Name.</span></span> <span data-ttu-id="038ee-124">탄력적 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="038ee-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="038ee-125">예제의</span><span class="sxs-lookup"><span data-stu-id="038ee-125">EXAMPLES</span></span>

### <span data-ttu-id="038ee-126">예제 1: 서버에 대 한 권장 사항 보기</span><span class="sxs-lookup"><span data-stu-id="038ee-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="038ee-127">이 명령은 Server01 이라는 서버에 대 한 탄력적 풀 권장 사항을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="038ee-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="038ee-128">변수</span><span class="sxs-lookup"><span data-stu-id="038ee-128">PARAMETERS</span></span>

### <span data-ttu-id="038ee-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="038ee-129">-ResourceGroupName</span></span>
<span data-ttu-id="038ee-130">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="038ee-130">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="038ee-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="038ee-131">-ServerName</span></span>
<span data-ttu-id="038ee-132">이 cmdlet이 권장 사항을 제공 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="038ee-132">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="038ee-133">-확인</span><span class="sxs-lookup"><span data-stu-id="038ee-133">-Confirm</span></span>
<span data-ttu-id="038ee-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="038ee-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="038ee-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="038ee-135">-WhatIf</span></span>
<span data-ttu-id="038ee-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="038ee-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="038ee-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="038ee-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="038ee-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="038ee-138">-DefaultProfile</span></span>
<span data-ttu-id="038ee-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="038ee-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="038ee-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="038ee-140">CommonParameters</span></span>
<span data-ttu-id="038ee-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="038ee-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="038ee-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="038ee-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="038ee-143">입력</span><span class="sxs-lookup"><span data-stu-id="038ee-143">INPUTS</span></span>

## <span data-ttu-id="038ee-144">출력</span><span class="sxs-lookup"><span data-stu-id="038ee-144">OUTPUTS</span></span>

## <span data-ttu-id="038ee-145">상속자</span><span class="sxs-lookup"><span data-stu-id="038ee-145">NOTES</span></span>

## <span data-ttu-id="038ee-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="038ee-146">RELATED LINKS</span></span>

