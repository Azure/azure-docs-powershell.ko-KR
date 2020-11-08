---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
ms.openlocfilehash: b9eebe26e64e9a7ce2497cdf9984ca6dabb062e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879382"
---
# <span data-ttu-id="99aa0-101">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="99aa0-101">Set-AzDataFactoryGateway</span></span>

## <span data-ttu-id="99aa0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99aa0-102">SYNOPSIS</span></span>
<span data-ttu-id="99aa0-103">Azure Data Factory의 게이트웨이에 대 한 설명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99aa0-103">Sets the description for a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="99aa0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="99aa0-104">SYNTAX</span></span>

### <span data-ttu-id="99aa0-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="99aa0-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99aa0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="99aa0-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99aa0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="99aa0-107">DESCRIPTION</span></span>
<span data-ttu-id="99aa0-108">**AzDataFactoryGateway** Cmdlet은 Azure Data Factory에서 지정 된 게이트웨이에 대 한 설명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99aa0-108">The **Set-AzDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="99aa0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="99aa0-109">EXAMPLES</span></span>

### <span data-ttu-id="99aa0-110">예제 1: 게이트웨이에 대 한 설명 설정</span><span class="sxs-lookup"><span data-stu-id="99aa0-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name            : ContosoGateway
Description     : my gateway
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:31:09 AM
RegisterTime    : 8/22/2014 1:31:37 AM
LastConnectTime : 8/22/2014 1:41:41 AM
ExpiryTime      :
```

<span data-ttu-id="99aa0-111">이 명령은 WikiADF 이라는 data factory의 ContosoGateway 이라는 게이트웨이에 대 한 설명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99aa0-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="99aa0-112">Description 매개 변수는 새 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99aa0-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="99aa0-113">변수</span><span class="sxs-lookup"><span data-stu-id="99aa0-113">PARAMETERS</span></span>

### <span data-ttu-id="99aa0-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="99aa0-114">-DataFactory</span></span>
<span data-ttu-id="99aa0-115">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99aa0-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="99aa0-116">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 게이트웨이에 대 한 설명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99aa0-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="99aa0-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="99aa0-117">-DataFactoryName</span></span>
<span data-ttu-id="99aa0-118">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99aa0-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="99aa0-119">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 게이트웨이에 대 한 설명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99aa0-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="99aa0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99aa0-120">-DefaultProfile</span></span>
<span data-ttu-id="99aa0-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="99aa0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99aa0-122">-설명</span><span class="sxs-lookup"><span data-stu-id="99aa0-122">-Description</span></span>
<span data-ttu-id="99aa0-123">게이트웨이에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99aa0-123">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99aa0-124">-이름</span><span class="sxs-lookup"><span data-stu-id="99aa0-124">-Name</span></span>
<span data-ttu-id="99aa0-125">설명을 설정할 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99aa0-125">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="99aa0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99aa0-126">-ResourceGroupName</span></span>
<span data-ttu-id="99aa0-127">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99aa0-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="99aa0-128">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 게이트웨이에 대 한 설명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99aa0-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="99aa0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99aa0-129">CommonParameters</span></span>
<span data-ttu-id="99aa0-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="99aa0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99aa0-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99aa0-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99aa0-132">입력</span><span class="sxs-lookup"><span data-stu-id="99aa0-132">INPUTS</span></span>

### <span data-ttu-id="99aa0-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="99aa0-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="99aa0-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="99aa0-134">System.String</span></span>

## <span data-ttu-id="99aa0-135">출력</span><span class="sxs-lookup"><span data-stu-id="99aa0-135">OUTPUTS</span></span>

### <span data-ttu-id="99aa0-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="99aa0-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="99aa0-137">상속자</span><span class="sxs-lookup"><span data-stu-id="99aa0-137">NOTES</span></span>
* <span data-ttu-id="99aa0-138">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="99aa0-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="99aa0-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99aa0-139">RELATED LINKS</span></span>

[<span data-ttu-id="99aa0-140">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="99aa0-140">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="99aa0-141">새로운 AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="99aa0-141">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="99aa0-142">제거-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="99aa0-142">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

