---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/update-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
ms.openlocfilehash: c80716e53b6f3aec6c9196baebbcd333aed1582c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964827"
---
# <span data-ttu-id="03b99-101">Update-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="03b99-101">Update-AzDataFactoryV2</span></span>

## <span data-ttu-id="03b99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03b99-102">SYNOPSIS</span></span>
<span data-ttu-id="03b99-103">데이터 팩터리의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="03b99-103">Updates the properties of a data factory.</span></span>

## <span data-ttu-id="03b99-104">구문</span><span class="sxs-lookup"><span data-stu-id="03b99-104">SYNTAX</span></span>

### <span data-ttu-id="03b99-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="03b99-105">ByFactoryName (Default)</span></span>
```
Update-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03b99-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="03b99-106">ByFactoryObject</span></span>
```
Update-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03b99-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="03b99-107">ByResourceId</span></span>
```
Update-AzDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03b99-108">설명</span><span class="sxs-lookup"><span data-stu-id="03b99-108">DESCRIPTION</span></span>
<span data-ttu-id="03b99-109">**Update-AzDataFactoryV2** cmdlet은 데이터 팩터리의 태그 또는 ID 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="03b99-109">The **Update-AzDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="03b99-110">예제</span><span class="sxs-lookup"><span data-stu-id="03b99-110">EXAMPLES</span></span>

### <span data-ttu-id="03b99-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="03b99-111">Example 1</span></span>
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

<span data-ttu-id="03b99-112">이 명령은 myTagValue 값으로 myNewTagName이라는 태그가 포함된 사전으로 팩터리 WikiADF의 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="03b99-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="03b99-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="03b99-113">PARAMETERS</span></span>

### <span data-ttu-id="03b99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03b99-114">-DefaultProfile</span></span>
<span data-ttu-id="03b99-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03b99-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03b99-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03b99-116">-InputObject</span></span>
<span data-ttu-id="03b99-117">데이터 팩터리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="03b99-117">The data factory object.</span></span>

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

### <span data-ttu-id="03b99-118">-Name</span><span class="sxs-lookup"><span data-stu-id="03b99-118">-Name</span></span>
<span data-ttu-id="03b99-119">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03b99-119">The data factory name.</span></span>

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

### <span data-ttu-id="03b99-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03b99-120">-ResourceGroupName</span></span>
<span data-ttu-id="03b99-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03b99-121">The resource group name.</span></span>

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

### <span data-ttu-id="03b99-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03b99-122">-ResourceId</span></span>
<span data-ttu-id="03b99-123">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="03b99-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="03b99-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="03b99-124">-Tag</span></span>
<span data-ttu-id="03b99-125">데이터 팩터리의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="03b99-125">The tags of the data factory.</span></span>

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

### <span data-ttu-id="03b99-126">-확인</span><span class="sxs-lookup"><span data-stu-id="03b99-126">-Confirm</span></span>
<span data-ttu-id="03b99-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="03b99-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03b99-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03b99-128">-WhatIf</span></span>
<span data-ttu-id="03b99-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="03b99-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03b99-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03b99-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03b99-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03b99-131">CommonParameters</span></span>
<span data-ttu-id="03b99-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="03b99-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03b99-133">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="03b99-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03b99-134">입력</span><span class="sxs-lookup"><span data-stu-id="03b99-134">INPUTS</span></span>

### <span data-ttu-id="03b99-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="03b99-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="03b99-136">System.String</span><span class="sxs-lookup"><span data-stu-id="03b99-136">System.String</span></span>

## <span data-ttu-id="03b99-137">출력</span><span class="sxs-lookup"><span data-stu-id="03b99-137">OUTPUTS</span></span>

### <span data-ttu-id="03b99-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="03b99-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="03b99-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="03b99-139">NOTES</span></span>

## <span data-ttu-id="03b99-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03b99-140">RELATED LINKS</span></span>
