---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
ms.openlocfilehash: 450a833656f6508f70ebd97f5387075c1711c5f9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94215037"
---
# <span data-ttu-id="3bd9a-101">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="3bd9a-101">New-AzDataFactory</span></span>

## <span data-ttu-id="3bd9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bd9a-102">SYNOPSIS</span></span>
<span data-ttu-id="3bd9a-103">Data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3bd9a-103">Creates a data factory.</span></span>

## <span data-ttu-id="3bd9a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3bd9a-104">SYNTAX</span></span>

```
New-AzDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3bd9a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3bd9a-105">DESCRIPTION</span></span>
<span data-ttu-id="3bd9a-106">**AzDataFactory** cmdlet은 지정 된 리소스 그룹 이름 및 위치를 사용 하 여 데이터 팩터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3bd9a-106">The **New-AzDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="3bd9a-107">다음 순서 대로 이러한 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd9a-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="3bd9a-108">Data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3bd9a-108">Create a data factory.</span></span> 
- <span data-ttu-id="3bd9a-109">연결 된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3bd9a-109">Create linked services.</span></span> 
- <span data-ttu-id="3bd9a-110">데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3bd9a-110">Create datasets.</span></span> 
- <span data-ttu-id="3bd9a-111">파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3bd9a-111">Create a pipeline.</span></span>

## <span data-ttu-id="3bd9a-112">예제의</span><span class="sxs-lookup"><span data-stu-id="3bd9a-112">EXAMPLES</span></span>

### <span data-ttu-id="3bd9a-113">예제 1: data factory 만들기</span><span class="sxs-lookup"><span data-stu-id="3bd9a-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="3bd9a-114">이 명령은 WestUS 위치에서 ADF 라는 리소스 그룹에 WikiADF 이라는 data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3bd9a-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="3bd9a-115">변수</span><span class="sxs-lookup"><span data-stu-id="3bd9a-115">PARAMETERS</span></span>

### <span data-ttu-id="3bd9a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bd9a-116">-DefaultProfile</span></span>
<span data-ttu-id="3bd9a-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3bd9a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3bd9a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3bd9a-118">-Force</span></span>
<span data-ttu-id="3bd9a-119">이 cmdlet이 확인 메시지 없이 기존 data factory를 대체 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3bd9a-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="3bd9a-120">-위치</span><span class="sxs-lookup"><span data-stu-id="3bd9a-120">-Location</span></span>
<span data-ttu-id="3bd9a-121">Data factory의 위치 (예: WestUS 또는 Ea Us)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd9a-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="3bd9a-122">현재 WestUS만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3bd9a-122">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="3bd9a-123">-이름</span><span class="sxs-lookup"><span data-stu-id="3bd9a-123">-Name</span></span>
<span data-ttu-id="3bd9a-124">만들 데이터 팩터리의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd9a-124">Specifies the name of the data factory to create.</span></span>

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

### <span data-ttu-id="3bd9a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bd9a-125">-ResourceGroupName</span></span>
<span data-ttu-id="3bd9a-126">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd9a-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3bd9a-127">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3bd9a-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3bd9a-128">태그</span><span class="sxs-lookup"><span data-stu-id="3bd9a-128">-Tag</span></span>
<span data-ttu-id="3bd9a-129">Data factory의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="3bd9a-129">The tags of the data factory.</span></span>

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

### <span data-ttu-id="3bd9a-130">-확인</span><span class="sxs-lookup"><span data-stu-id="3bd9a-130">-Confirm</span></span>
<span data-ttu-id="3bd9a-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd9a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bd9a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bd9a-132">-WhatIf</span></span>
<span data-ttu-id="3bd9a-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3bd9a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bd9a-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3bd9a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bd9a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd9a-135">CommonParameters</span></span>
<span data-ttu-id="3bd9a-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bd9a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd9a-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bd9a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd9a-138">입력</span><span class="sxs-lookup"><span data-stu-id="3bd9a-138">INPUTS</span></span>

### <span data-ttu-id="3bd9a-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3bd9a-139">System.String</span></span>

### <span data-ttu-id="3bd9a-140">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="3bd9a-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3bd9a-141">출력</span><span class="sxs-lookup"><span data-stu-id="3bd9a-141">OUTPUTS</span></span>

### <span data-ttu-id="3bd9a-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3bd9a-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="3bd9a-143">상속자</span><span class="sxs-lookup"><span data-stu-id="3bd9a-143">NOTES</span></span>
* <span data-ttu-id="3bd9a-144">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="3bd9a-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3bd9a-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3bd9a-145">RELATED LINKS</span></span>

[<span data-ttu-id="3bd9a-146">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="3bd9a-146">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="3bd9a-147">제거-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="3bd9a-147">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


