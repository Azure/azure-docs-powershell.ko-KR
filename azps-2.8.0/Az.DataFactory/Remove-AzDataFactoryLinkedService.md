---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
ms.openlocfilehash: a0e8a131b0a66c3887ecea7054a2f13b75e7f598
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697005"
---
# <span data-ttu-id="d1d13-101">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="d1d13-101">Remove-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="d1d13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1d13-102">SYNOPSIS</span></span>
<span data-ttu-id="d1d13-103">Azure Data Factory에서 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d13-103">Removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="d1d13-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1d13-104">SYNTAX</span></span>

### <span data-ttu-id="d1d13-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d1d13-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1d13-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d1d13-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1d13-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d1d13-107">DESCRIPTION</span></span>
<span data-ttu-id="d1d13-108">**AzDataFactoryLinkedService** Cmdlet은 Azure Data Factory에서 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d13-108">The **Remove-AzDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="d1d13-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d1d13-109">EXAMPLES</span></span>

### <span data-ttu-id="d1d13-110">예제 1: 연결 된 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="d1d13-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="d1d13-111">이 명령은 WikiADF 이라는 data factory에서 LinkedServiceTest 라는 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d13-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="d1d13-112">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d13-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="d1d13-113">변수</span><span class="sxs-lookup"><span data-stu-id="d1d13-113">PARAMETERS</span></span>

### <span data-ttu-id="d1d13-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d1d13-114">-DataFactory</span></span>
<span data-ttu-id="d1d13-115">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d13-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d1d13-116">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d13-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d1d13-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d1d13-117">-DataFactoryName</span></span>
<span data-ttu-id="d1d13-118">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d13-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d1d13-119">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d13-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1d13-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1d13-120">-DefaultProfile</span></span>
<span data-ttu-id="d1d13-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d1d13-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1d13-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d1d13-122">-Force</span></span>
<span data-ttu-id="d1d13-123">이 cmdlet이 확인을 묻지 않고 연결 된 서비스를 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d1d13-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="d1d13-124">-이름</span><span class="sxs-lookup"><span data-stu-id="d1d13-124">-Name</span></span>
<span data-ttu-id="d1d13-125">제거할 연결 된 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d13-125">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1d13-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1d13-126">-ResourceGroupName</span></span>
<span data-ttu-id="d1d13-127">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d13-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d1d13-128">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d13-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d1d13-129">-확인</span><span class="sxs-lookup"><span data-stu-id="d1d13-129">-Confirm</span></span>
<span data-ttu-id="d1d13-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d13-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1d13-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1d13-131">-WhatIf</span></span>
<span data-ttu-id="d1d13-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d1d13-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1d13-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1d13-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1d13-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1d13-134">CommonParameters</span></span>
<span data-ttu-id="d1d13-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d13-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1d13-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1d13-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1d13-137">입력</span><span class="sxs-lookup"><span data-stu-id="d1d13-137">INPUTS</span></span>

### <span data-ttu-id="d1d13-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d1d13-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="d1d13-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d1d13-139">System.String</span></span>

## <span data-ttu-id="d1d13-140">출력</span><span class="sxs-lookup"><span data-stu-id="d1d13-140">OUTPUTS</span></span>

### <span data-ttu-id="d1d13-141">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="d1d13-141">System.Void</span></span>

## <span data-ttu-id="d1d13-142">상속자</span><span class="sxs-lookup"><span data-stu-id="d1d13-142">NOTES</span></span>
* <span data-ttu-id="d1d13-143">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="d1d13-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d1d13-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1d13-144">RELATED LINKS</span></span>

[<span data-ttu-id="d1d13-145">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="d1d13-145">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="d1d13-146">새로운 AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="d1d13-146">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)


