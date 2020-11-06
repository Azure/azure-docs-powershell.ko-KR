---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: f0fcfd8a99bd28f01077257e48c0dc9662973751
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525156"
---
# <span data-ttu-id="6fb54-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6fb54-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="6fb54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fb54-102">SYNOPSIS</span></span>
<span data-ttu-id="6fb54-103">Data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6fb54-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fb54-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6fb54-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6fb54-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6fb54-105">DESCRIPTION</span></span>
<span data-ttu-id="6fb54-106">**AzureRmDataFactoryV2** cmdlet은 지정 된 리소스 그룹 이름 및 위치를 사용 하 여 데이터 팩터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6fb54-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="6fb54-107">다음 순서 대로 이러한 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fb54-107">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="6fb54-108">예제의</span><span class="sxs-lookup"><span data-stu-id="6fb54-108">EXAMPLES</span></span>

### <span data-ttu-id="6fb54-109">예제 1: data factory 만들기</span><span class="sxs-lookup"><span data-stu-id="6fb54-109">Example 1: Create a data factory</span></span>
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

<span data-ttu-id="6fb54-110">이 명령은 WestUS 위치에서 ADF 라는 리소스 그룹에 WikiADF 이라는 data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6fb54-110">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="6fb54-111">변수</span><span class="sxs-lookup"><span data-stu-id="6fb54-111">PARAMETERS</span></span>

### <span data-ttu-id="6fb54-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fb54-112">-DefaultProfile</span></span>
<span data-ttu-id="6fb54-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6fb54-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fb54-114">-Force</span><span class="sxs-lookup"><span data-stu-id="6fb54-114">-Force</span></span>
<span data-ttu-id="6fb54-115">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fb54-115">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6fb54-116">-위치</span><span class="sxs-lookup"><span data-stu-id="6fb54-116">-Location</span></span>
<span data-ttu-id="6fb54-117">이 지역에 데이터 팩터리가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6fb54-117">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="6fb54-118">-이름</span><span class="sxs-lookup"><span data-stu-id="6fb54-118">-Name</span></span>
<span data-ttu-id="6fb54-119">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6fb54-119">The data factory name.</span></span>

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

### <span data-ttu-id="6fb54-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fb54-120">-ResourceGroupName</span></span>
<span data-ttu-id="6fb54-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6fb54-121">The resource group name.</span></span>

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

### <span data-ttu-id="6fb54-122">태그</span><span class="sxs-lookup"><span data-stu-id="6fb54-122">-Tag</span></span>
<span data-ttu-id="6fb54-123">Data factory의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="6fb54-123">The tags of the data factory.</span></span>

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

### <span data-ttu-id="6fb54-124">-확인</span><span class="sxs-lookup"><span data-stu-id="6fb54-124">-Confirm</span></span>
<span data-ttu-id="6fb54-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fb54-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fb54-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fb54-126">-WhatIf</span></span>
<span data-ttu-id="6fb54-127">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6fb54-127">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="6fb54-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fb54-128">CommonParameters</span></span>
<span data-ttu-id="6fb54-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fb54-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fb54-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fb54-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fb54-131">입력</span><span class="sxs-lookup"><span data-stu-id="6fb54-131">INPUTS</span></span>

### <span data-ttu-id="6fb54-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6fb54-132">System.String</span></span>
<span data-ttu-id="6fb54-133">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="6fb54-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6fb54-134">출력</span><span class="sxs-lookup"><span data-stu-id="6fb54-134">OUTPUTS</span></span>

### <span data-ttu-id="6fb54-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6fb54-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="6fb54-136">상속자</span><span class="sxs-lookup"><span data-stu-id="6fb54-136">NOTES</span></span>
<span data-ttu-id="6fb54-137">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="6fb54-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6fb54-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6fb54-138">RELATED LINKS</span></span>

[<span data-ttu-id="6fb54-139">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6fb54-139">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="6fb54-140">제거-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6fb54-140">Remove-AzureRmDataFactoryV2</span></span>]()
