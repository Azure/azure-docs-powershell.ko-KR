---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
ms.openlocfilehash: 57c0a05c5b0f279fa7c9f06cd561385de87698bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493496"
---
# <span data-ttu-id="642b1-101">Update-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="642b1-101">Update-AzDataFactoryV2</span></span>

## <span data-ttu-id="642b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="642b1-102">SYNOPSIS</span></span>
<span data-ttu-id="642b1-103">데이터 팩터리의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="642b1-103">Updates the properties of a data factory.</span></span>

## <span data-ttu-id="642b1-104">구문</span><span class="sxs-lookup"><span data-stu-id="642b1-104">SYNTAX</span></span>

### <span data-ttu-id="642b1-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="642b1-105">ByFactoryName (Default)</span></span>
```
Update-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="642b1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="642b1-106">ByFactoryObject</span></span>
```
Update-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="642b1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="642b1-107">ByResourceId</span></span>
```
Update-AzDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="642b1-108">설명</span><span class="sxs-lookup"><span data-stu-id="642b1-108">DESCRIPTION</span></span>
<span data-ttu-id="642b1-109">**Update-AzDataFactoryV2** cmdlet은 데이터 팩터리의 태그 또는 ID 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="642b1-109">The **Update-AzDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="642b1-110">예제</span><span class="sxs-lookup"><span data-stu-id="642b1-110">EXAMPLES</span></span>

### <span data-ttu-id="642b1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="642b1-111">Example 1</span></span>
```
PS C:\> Update-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Tag @{myNewTagName = "myTagValue"}

Confirm
Are you sure you want to update properties of the data factory 'WikiADF' in resource group 'ADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


DataFactoryName   : WikiADF
DataFactoryId     : /subscriptions/1e42591f-1f0c-4c5a-b7f2-a268f6105ec5/resourceGroups/adf/providers/Microsoft.DataF
                    actory/factories/wikiadf
ResourceGroupName : ADF
Location          : EastUS
Tags              : {[myNewTagName, myTagValue]}
Identity          :
ProvisioningState : Succeeded
```

<span data-ttu-id="642b1-112">이 명령은 myTagValue 값이 있는 myNewTagName이라는 태그가 포함된 사전으로 팩터리 WikiADF에 대한 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="642b1-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="642b1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="642b1-113">PARAMETERS</span></span>

### <span data-ttu-id="642b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="642b1-114">-DefaultProfile</span></span>
<span data-ttu-id="642b1-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="642b1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="642b1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="642b1-116">-InputObject</span></span>
<span data-ttu-id="642b1-117">데이터 팩터리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="642b1-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="642b1-118">-Name</span><span class="sxs-lookup"><span data-stu-id="642b1-118">-Name</span></span>
<span data-ttu-id="642b1-119">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="642b1-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642b1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="642b1-120">-ResourceGroupName</span></span>
<span data-ttu-id="642b1-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="642b1-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642b1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="642b1-122">-ResourceId</span></span>
<span data-ttu-id="642b1-123">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="642b1-123">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="642b1-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="642b1-124">-Tag</span></span>
<span data-ttu-id="642b1-125">데이터 팩터리의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="642b1-125">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642b1-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="642b1-126">-Confirm</span></span>
<span data-ttu-id="642b1-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="642b1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="642b1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="642b1-128">-WhatIf</span></span>
<span data-ttu-id="642b1-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="642b1-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="642b1-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="642b1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="642b1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="642b1-131">CommonParameters</span></span>
<span data-ttu-id="642b1-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="642b1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="642b1-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="642b1-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="642b1-134">입력</span><span class="sxs-lookup"><span data-stu-id="642b1-134">INPUTS</span></span>

### <span data-ttu-id="642b1-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="642b1-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="642b1-136">System.String</span><span class="sxs-lookup"><span data-stu-id="642b1-136">System.String</span></span>

## <span data-ttu-id="642b1-137">출력</span><span class="sxs-lookup"><span data-stu-id="642b1-137">OUTPUTS</span></span>

### <span data-ttu-id="642b1-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="642b1-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="642b1-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="642b1-139">NOTES</span></span>

## <span data-ttu-id="642b1-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="642b1-140">RELATED LINKS</span></span>
