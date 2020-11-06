---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
ms.openlocfilehash: 13e9a8de97ee19e53c31a76516fef7c9fcfcaedd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525543"
---
# <span data-ttu-id="9b106-101">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="9b106-101">New-AzureRmDataFactory</span></span>

## <span data-ttu-id="9b106-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b106-102">SYNOPSIS</span></span>
<span data-ttu-id="9b106-103">Data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b106-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b106-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b106-104">SYNTAX</span></span>

```
New-AzureRmDataFactory [-Name] <String> [-Location] <String> [[-Tags] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b106-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9b106-105">DESCRIPTION</span></span>
<span data-ttu-id="9b106-106">**AzureRmDataFactory** cmdlet은 지정 된 리소스 그룹 이름 및 위치를 사용 하 여 데이터 팩터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b106-106">The **New-AzureRmDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="9b106-107">다음 순서 대로 이러한 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b106-107">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="9b106-108">Data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b106-108">Create a data factory.</span></span> 
- <span data-ttu-id="9b106-109">연결 된 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b106-109">Create linked services.</span></span> 
- <span data-ttu-id="9b106-110">데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b106-110">Create datasets.</span></span> 
- <span data-ttu-id="9b106-111">파이프라인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b106-111">Create a pipeline.</span></span>

## <span data-ttu-id="9b106-112">예제의</span><span class="sxs-lookup"><span data-stu-id="9b106-112">EXAMPLES</span></span>

### <span data-ttu-id="9b106-113">예제 1: data factory 만들기</span><span class="sxs-lookup"><span data-stu-id="9b106-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="9b106-114">이 명령은 WestUS 위치에서 ADF 라는 리소스 그룹에 WikiADF 이라는 data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b106-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="9b106-115">변수</span><span class="sxs-lookup"><span data-stu-id="9b106-115">PARAMETERS</span></span>

### <span data-ttu-id="9b106-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9b106-116">-Force</span></span>
<span data-ttu-id="9b106-117">이 cmdlet이 확인 메시지 없이 기존 data factory를 대체 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9b106-117">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="9b106-118">-위치</span><span class="sxs-lookup"><span data-stu-id="9b106-118">-Location</span></span>
<span data-ttu-id="9b106-119">Data factory의 위치 (예: WestUS 또는 Ea Us)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b106-119">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="9b106-120">현재 WestUS만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b106-120">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="9b106-121">-이름</span><span class="sxs-lookup"><span data-stu-id="9b106-121">-Name</span></span>
<span data-ttu-id="9b106-122">만들 데이터 팩터리의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b106-122">Specifies the name of the data factory to create.</span></span>

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

### <span data-ttu-id="9b106-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b106-123">-ResourceGroupName</span></span>
<span data-ttu-id="9b106-124">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b106-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9b106-125">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b106-125">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9b106-126">태그</span><span class="sxs-lookup"><span data-stu-id="9b106-126">-Tags</span></span>
<span data-ttu-id="9b106-127">Data factory에 대 한 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b106-127">Specifies tags for the data factory.</span></span>

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

### <span data-ttu-id="9b106-128">-확인</span><span class="sxs-lookup"><span data-stu-id="9b106-128">-Confirm</span></span>
<span data-ttu-id="9b106-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b106-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b106-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b106-130">-WhatIf</span></span>
<span data-ttu-id="9b106-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b106-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b106-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b106-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b106-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b106-133">-DefaultProfile</span></span>
<span data-ttu-id="9b106-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b106-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b106-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b106-135">CommonParameters</span></span>
<span data-ttu-id="9b106-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b106-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b106-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b106-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b106-138">입력</span><span class="sxs-lookup"><span data-stu-id="9b106-138">INPUTS</span></span>

## <span data-ttu-id="9b106-139">출력</span><span class="sxs-lookup"><span data-stu-id="9b106-139">OUTPUTS</span></span>

### <span data-ttu-id="9b106-140">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9b106-140">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span></span>

## <span data-ttu-id="9b106-141">상속자</span><span class="sxs-lookup"><span data-stu-id="9b106-141">NOTES</span></span>
* <span data-ttu-id="9b106-142">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="9b106-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9b106-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b106-143">RELATED LINKS</span></span>

[<span data-ttu-id="9b106-144">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="9b106-144">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="9b106-145">제거-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="9b106-145">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)


