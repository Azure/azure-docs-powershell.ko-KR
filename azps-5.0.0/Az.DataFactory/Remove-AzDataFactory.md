---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
ms.openlocfilehash: 36c22a432d4e281600a1b718c1ac58a851fb7069
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306134"
---
# <span data-ttu-id="ed4b5-101">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="ed4b5-101">Remove-AzDataFactory</span></span>

## <span data-ttu-id="ed4b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed4b5-102">SYNOPSIS</span></span>
<span data-ttu-id="ed4b5-103">Data factory를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed4b5-103">Removes a data factory.</span></span>

## <span data-ttu-id="ed4b5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ed4b5-104">SYNTAX</span></span>

### <span data-ttu-id="ed4b5-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ed4b5-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed4b5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ed4b5-106">ByFactoryObject</span></span>
```
Remove-AzDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed4b5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ed4b5-107">DESCRIPTION</span></span>
<span data-ttu-id="ed4b5-108">**AzDataFactory** cmdlet은 data factory를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed4b5-108">The **Remove-AzDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="ed4b5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ed4b5-109">EXAMPLES</span></span>

### <span data-ttu-id="ed4b5-110">예제 1: data factory 제거</span><span class="sxs-lookup"><span data-stu-id="ed4b5-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="ed4b5-111">이 명령은 ADF 라는 리소스 그룹에서 WikiADF 이라는 data factory를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed4b5-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="ed4b5-112">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed4b5-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="ed4b5-113">변수</span><span class="sxs-lookup"><span data-stu-id="ed4b5-113">PARAMETERS</span></span>

### <span data-ttu-id="ed4b5-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ed4b5-114">-DataFactory</span></span>
<span data-ttu-id="ed4b5-115">제거할 **PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed4b5-115">Specifies the **PSDataFactory** object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed4b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed4b5-116">-DefaultProfile</span></span>
<span data-ttu-id="ed4b5-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ed4b5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed4b5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ed4b5-118">-Force</span></span>
<span data-ttu-id="ed4b5-119">이 cmdlet이 확인을 묻지 않고 데이터 팩토리를 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ed4b5-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="ed4b5-120">-이름</span><span class="sxs-lookup"><span data-stu-id="ed4b5-120">-Name</span></span>
<span data-ttu-id="ed4b5-121">제거할 데이터 팩터리의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed4b5-121">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed4b5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed4b5-122">-ResourceGroupName</span></span>
<span data-ttu-id="ed4b5-123">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed4b5-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ed4b5-124">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 데이터 팩터리를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed4b5-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed4b5-125">-확인</span><span class="sxs-lookup"><span data-stu-id="ed4b5-125">-Confirm</span></span>
<span data-ttu-id="ed4b5-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed4b5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed4b5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed4b5-127">-WhatIf</span></span>
<span data-ttu-id="ed4b5-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ed4b5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed4b5-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed4b5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed4b5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed4b5-130">CommonParameters</span></span>
<span data-ttu-id="ed4b5-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed4b5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed4b5-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed4b5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed4b5-133">입력</span><span class="sxs-lookup"><span data-stu-id="ed4b5-133">INPUTS</span></span>

### <span data-ttu-id="ed4b5-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ed4b5-134">System.String</span></span>

### <span data-ttu-id="ed4b5-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ed4b5-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="ed4b5-136">출력</span><span class="sxs-lookup"><span data-stu-id="ed4b5-136">OUTPUTS</span></span>

### <span data-ttu-id="ed4b5-137">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="ed4b5-137">System.Void</span></span>

## <span data-ttu-id="ed4b5-138">상속자</span><span class="sxs-lookup"><span data-stu-id="ed4b5-138">NOTES</span></span>
* <span data-ttu-id="ed4b5-139">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="ed4b5-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ed4b5-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed4b5-140">RELATED LINKS</span></span>

[<span data-ttu-id="ed4b5-141">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="ed4b5-141">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="ed4b5-142">새로운 AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="ed4b5-142">New-AzDataFactory</span></span>](./New-AzDataFactory.md)


