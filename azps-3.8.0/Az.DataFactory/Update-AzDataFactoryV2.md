---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
ms.openlocfilehash: 57c0a05c5b0f279fa7c9f06cd561385de87698bf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879306"
---
# <span data-ttu-id="24945-101">Update-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="24945-101">Update-AzDataFactoryV2</span></span>

## <span data-ttu-id="24945-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24945-102">SYNOPSIS</span></span>
<span data-ttu-id="24945-103">Data factory의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="24945-103">Updates the properties of a data factory.</span></span>

## <span data-ttu-id="24945-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24945-104">SYNTAX</span></span>

### <span data-ttu-id="24945-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="24945-105">ByFactoryName (Default)</span></span>
```
Update-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24945-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="24945-106">ByFactoryObject</span></span>
```
Update-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24945-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="24945-107">ByResourceId</span></span>
```
Update-AzDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24945-108">설명은</span><span class="sxs-lookup"><span data-stu-id="24945-108">DESCRIPTION</span></span>
<span data-ttu-id="24945-109">**업데이트 AzDataFactoryV2** cmdlet은 data factory의 태그 또는 id 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="24945-109">The **Update-AzDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="24945-110">예제의</span><span class="sxs-lookup"><span data-stu-id="24945-110">EXAMPLES</span></span>

### <span data-ttu-id="24945-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="24945-111">Example 1</span></span>
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

<span data-ttu-id="24945-112">이 명령은 factory WikiADF의 태그를 value myTagValue 이라는 myNewTagName 라는 태그가 포함 된 dictionary로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="24945-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="24945-113">변수</span><span class="sxs-lookup"><span data-stu-id="24945-113">PARAMETERS</span></span>

### <span data-ttu-id="24945-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24945-114">-DefaultProfile</span></span>
<span data-ttu-id="24945-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24945-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24945-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24945-116">-InputObject</span></span>
<span data-ttu-id="24945-117">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="24945-117">The data factory object.</span></span>

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

### <span data-ttu-id="24945-118">-이름</span><span class="sxs-lookup"><span data-stu-id="24945-118">-Name</span></span>
<span data-ttu-id="24945-119">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24945-119">The data factory name.</span></span>

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

### <span data-ttu-id="24945-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24945-120">-ResourceGroupName</span></span>
<span data-ttu-id="24945-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24945-121">The resource group name.</span></span>

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

### <span data-ttu-id="24945-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24945-122">-ResourceId</span></span>
<span data-ttu-id="24945-123">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="24945-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="24945-124">태그</span><span class="sxs-lookup"><span data-stu-id="24945-124">-Tag</span></span>
<span data-ttu-id="24945-125">Data factory의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="24945-125">The tags of the data factory.</span></span>

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

### <span data-ttu-id="24945-126">-확인</span><span class="sxs-lookup"><span data-stu-id="24945-126">-Confirm</span></span>
<span data-ttu-id="24945-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24945-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24945-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24945-128">-WhatIf</span></span>
<span data-ttu-id="24945-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24945-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24945-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24945-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24945-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24945-131">CommonParameters</span></span>
<span data-ttu-id="24945-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24945-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24945-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24945-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24945-134">입력</span><span class="sxs-lookup"><span data-stu-id="24945-134">INPUTS</span></span>

### <span data-ttu-id="24945-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="24945-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="24945-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="24945-136">System.String</span></span>

## <span data-ttu-id="24945-137">출력</span><span class="sxs-lookup"><span data-stu-id="24945-137">OUTPUTS</span></span>

### <span data-ttu-id="24945-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="24945-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="24945-139">상속자</span><span class="sxs-lookup"><span data-stu-id="24945-139">NOTES</span></span>

## <span data-ttu-id="24945-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24945-140">RELATED LINKS</span></span>