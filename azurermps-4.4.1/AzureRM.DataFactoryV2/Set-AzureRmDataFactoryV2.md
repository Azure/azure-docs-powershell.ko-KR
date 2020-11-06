---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 8dc191223d5ec17856605c7640d324cc2ee3794e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538212"
---
# <span data-ttu-id="554ff-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="554ff-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="554ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="554ff-102">SYNOPSIS</span></span>
<span data-ttu-id="554ff-103">Data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="554ff-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="554ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="554ff-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
[[-Tag] <Hashtable>] [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="554ff-105">설명은</span><span class="sxs-lookup"><span data-stu-id="554ff-105">DESCRIPTION</span></span>
<span data-ttu-id="554ff-106">**AzureRmDataFactoryV2** cmdlet은 지정 된 리소스 그룹 이름 및 위치를 사용 하 여 데이터 팩터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="554ff-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="554ff-107">다음 순서 대로 이러한 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="554ff-107">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="554ff-108">예제의</span><span class="sxs-lookup"><span data-stu-id="554ff-108">EXAMPLES</span></span>

### <span data-ttu-id="554ff-109">예제 1: data factory 만들기</span><span class="sxs-lookup"><span data-stu-id="554ff-109">Example 1: Create a data factory</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

```

<span data-ttu-id="554ff-110">이 명령은 WestUS 위치에서 ADF 라는 리소스 그룹에 WikiADF 이라는 data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="554ff-110">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="554ff-111">변수</span><span class="sxs-lookup"><span data-stu-id="554ff-111">PARAMETERS</span></span>

### <span data-ttu-id="554ff-112">-확인</span><span class="sxs-lookup"><span data-stu-id="554ff-112">-Confirm</span></span>
<span data-ttu-id="554ff-113">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="554ff-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="554ff-114">-Force</span><span class="sxs-lookup"><span data-stu-id="554ff-114">-Force</span></span>
<span data-ttu-id="554ff-115">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="554ff-115">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="554ff-116">-위치</span><span class="sxs-lookup"><span data-stu-id="554ff-116">-Location</span></span>
<span data-ttu-id="554ff-117">이 지역에 데이터 팩터리가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="554ff-117">The data factory is created in this region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="554ff-118">-이름</span><span class="sxs-lookup"><span data-stu-id="554ff-118">-Name</span></span>
<span data-ttu-id="554ff-119">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="554ff-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="554ff-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="554ff-120">-ResourceGroupName</span></span>
<span data-ttu-id="554ff-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="554ff-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="554ff-122">태그</span><span class="sxs-lookup"><span data-stu-id="554ff-122">-Tag</span></span>
<span data-ttu-id="554ff-123">Data factory의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="554ff-123">The tags of the data factory.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="554ff-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="554ff-124">-WhatIf</span></span>
<span data-ttu-id="554ff-125">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="554ff-125">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="554ff-126">입력</span><span class="sxs-lookup"><span data-stu-id="554ff-126">INPUTS</span></span>

### <span data-ttu-id="554ff-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="554ff-127">System.String</span></span>
<span data-ttu-id="554ff-128">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="554ff-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="554ff-129">출력</span><span class="sxs-lookup"><span data-stu-id="554ff-129">OUTPUTS</span></span>

### <span data-ttu-id="554ff-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="554ff-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="554ff-131">상속자</span><span class="sxs-lookup"><span data-stu-id="554ff-131">NOTES</span></span>
<span data-ttu-id="554ff-132">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="554ff-132">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="554ff-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="554ff-133">RELATED LINKS</span></span>
[<span data-ttu-id="554ff-134">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="554ff-134">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="554ff-135">제거-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="554ff-135">Remove-AzureRmDataFactoryV2</span></span>]()
