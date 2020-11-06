---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: c50023cefbae9a9ba341eba22f40a421c37d12c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530370"
---
# <span data-ttu-id="497b6-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="497b6-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="497b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="497b6-102">SYNOPSIS</span></span>
<span data-ttu-id="497b6-103">Data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="497b6-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="497b6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="497b6-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="497b6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="497b6-105">DESCRIPTION</span></span>
<span data-ttu-id="497b6-106">**AzureRmDataFactoryV2** cmdlet은 지정 된 리소스 그룹 이름 및 위치를 사용 하 여 데이터 팩터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="497b6-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="497b6-107">다음 순서 대로 이러한 작업을 수행 합니다.--data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="497b6-107">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="497b6-108">--연결 된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="497b6-108">-- Create linked services.</span></span>
<span data-ttu-id="497b6-109">--데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="497b6-109">-- Create datasets.</span></span>
<span data-ttu-id="497b6-110">--파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="497b6-110">-- Create a pipeline.</span></span>

## <span data-ttu-id="497b6-111">예제의</span><span class="sxs-lookup"><span data-stu-id="497b6-111">EXAMPLES</span></span>

### <span data-ttu-id="497b6-112">예제 1: data factory 만들기</span><span class="sxs-lookup"><span data-stu-id="497b6-112">Example 1: Create a data factory</span></span>
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

<span data-ttu-id="497b6-113">이 명령은 WestUS 위치에서 ADF 라는 리소스 그룹에 WikiADF 이라는 data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="497b6-113">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="497b6-114">변수</span><span class="sxs-lookup"><span data-stu-id="497b6-114">PARAMETERS</span></span>

### <span data-ttu-id="497b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="497b6-115">-DefaultProfile</span></span>
<span data-ttu-id="497b6-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="497b6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="497b6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="497b6-117">-Force</span></span>
<span data-ttu-id="497b6-118">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="497b6-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="497b6-119">-위치</span><span class="sxs-lookup"><span data-stu-id="497b6-119">-Location</span></span>
<span data-ttu-id="497b6-120">이 지역에 데이터 팩터리가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="497b6-120">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="497b6-121">-이름</span><span class="sxs-lookup"><span data-stu-id="497b6-121">-Name</span></span>
<span data-ttu-id="497b6-122">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="497b6-122">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="497b6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="497b6-123">-ResourceGroupName</span></span>
<span data-ttu-id="497b6-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="497b6-124">The resource group name.</span></span>

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

### <span data-ttu-id="497b6-125">태그</span><span class="sxs-lookup"><span data-stu-id="497b6-125">-Tag</span></span>
<span data-ttu-id="497b6-126">Data factory의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="497b6-126">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="497b6-127">-확인</span><span class="sxs-lookup"><span data-stu-id="497b6-127">-Confirm</span></span>
<span data-ttu-id="497b6-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="497b6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="497b6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="497b6-129">-WhatIf</span></span>
<span data-ttu-id="497b6-130">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="497b6-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="497b6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="497b6-131">CommonParameters</span></span>
<span data-ttu-id="497b6-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="497b6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="497b6-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="497b6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="497b6-134">입력</span><span class="sxs-lookup"><span data-stu-id="497b6-134">INPUTS</span></span>

### <span data-ttu-id="497b6-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="497b6-135">System.String</span></span>

### <span data-ttu-id="497b6-136">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="497b6-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="497b6-137">출력</span><span class="sxs-lookup"><span data-stu-id="497b6-137">OUTPUTS</span></span>

### <span data-ttu-id="497b6-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="497b6-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="497b6-139">상속자</span><span class="sxs-lookup"><span data-stu-id="497b6-139">NOTES</span></span>
<span data-ttu-id="497b6-140">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="497b6-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="497b6-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="497b6-141">RELATED LINKS</span></span>

[<span data-ttu-id="497b6-142">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="497b6-142">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="497b6-143">제거-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="497b6-143">Remove-AzureRmDataFactoryV2</span></span>]()
