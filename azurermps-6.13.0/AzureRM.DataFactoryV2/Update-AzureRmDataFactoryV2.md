---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
ms.openlocfilehash: 09e13e973178444496604843336c8f483508c59e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530357"
---
# <span data-ttu-id="39ca3-101">Update-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="39ca3-101">Update-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="39ca3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="39ca3-103">Data factory의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ca3-103">Updates the properties of a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39ca3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="39ca3-104">SYNTAX</span></span>

### <span data-ttu-id="39ca3-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="39ca3-105">ByFactoryName (Default)</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39ca3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="39ca3-106">ByFactoryObject</span></span>
```
Update-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39ca3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="39ca3-107">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39ca3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="39ca3-108">DESCRIPTION</span></span>
<span data-ttu-id="39ca3-109">**업데이트 AzureRmDataFactoryV2** cmdlet은 data factory의 태그 또는 id 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ca3-109">The **Update-AzureRmDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="39ca3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="39ca3-110">EXAMPLES</span></span>

### <span data-ttu-id="39ca3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="39ca3-111">Example 1</span></span>
```
PS C:\> Update-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Tag @{myNewTagName = "myTagValue"}

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

<span data-ttu-id="39ca3-112">이 명령은 factory WikiADF의 태그를 value myTagValue 이라는 myNewTagName 라는 태그가 포함 된 dictionary로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ca3-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="39ca3-113">변수</span><span class="sxs-lookup"><span data-stu-id="39ca3-113">PARAMETERS</span></span>

### <span data-ttu-id="39ca3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39ca3-114">-DefaultProfile</span></span>
<span data-ttu-id="39ca3-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39ca3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39ca3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39ca3-116">-InputObject</span></span>
<span data-ttu-id="39ca3-117">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="39ca3-117">The data factory object.</span></span>

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

### <span data-ttu-id="39ca3-118">-이름</span><span class="sxs-lookup"><span data-stu-id="39ca3-118">-Name</span></span>
<span data-ttu-id="39ca3-119">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="39ca3-119">The data factory name.</span></span>

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

### <span data-ttu-id="39ca3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39ca3-120">-ResourceGroupName</span></span>
<span data-ttu-id="39ca3-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="39ca3-121">The resource group name.</span></span>

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

### <span data-ttu-id="39ca3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39ca3-122">-ResourceId</span></span>
<span data-ttu-id="39ca3-123">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="39ca3-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="39ca3-124">태그</span><span class="sxs-lookup"><span data-stu-id="39ca3-124">-Tag</span></span>
<span data-ttu-id="39ca3-125">Data factory의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="39ca3-125">The tags of the data factory.</span></span>

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

### <span data-ttu-id="39ca3-126">-확인</span><span class="sxs-lookup"><span data-stu-id="39ca3-126">-Confirm</span></span>
<span data-ttu-id="39ca3-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ca3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39ca3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39ca3-128">-WhatIf</span></span>
<span data-ttu-id="39ca3-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="39ca3-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39ca3-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39ca3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39ca3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39ca3-131">CommonParameters</span></span>
<span data-ttu-id="39ca3-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ca3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39ca3-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39ca3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39ca3-134">입력</span><span class="sxs-lookup"><span data-stu-id="39ca3-134">INPUTS</span></span>

### <span data-ttu-id="39ca3-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="39ca3-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="39ca3-136">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="39ca3-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="39ca3-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="39ca3-137">System.String</span></span>

## <span data-ttu-id="39ca3-138">출력</span><span class="sxs-lookup"><span data-stu-id="39ca3-138">OUTPUTS</span></span>

### <span data-ttu-id="39ca3-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="39ca3-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="39ca3-140">상속자</span><span class="sxs-lookup"><span data-stu-id="39ca3-140">NOTES</span></span>

## <span data-ttu-id="39ca3-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39ca3-141">RELATED LINKS</span></span>
