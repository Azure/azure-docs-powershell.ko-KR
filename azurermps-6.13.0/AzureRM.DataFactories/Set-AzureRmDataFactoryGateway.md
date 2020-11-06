---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
ms.openlocfilehash: c40999dfa9f1300502e8909a32eaf13a34d0bae0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532057"
---
# <span data-ttu-id="7b203-101">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="7b203-101">Set-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="7b203-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b203-102">SYNOPSIS</span></span>
<span data-ttu-id="7b203-103">Azure Data Factory의 게이트웨이에 대 한 설명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b203-103">Sets the description for a gateway in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b203-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7b203-104">SYNTAX</span></span>

### <span data-ttu-id="7b203-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="7b203-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b203-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7b203-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b203-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7b203-107">DESCRIPTION</span></span>
<span data-ttu-id="7b203-108">**AzureRmDataFactoryGateway** Cmdlet은 Azure Data Factory에서 지정 된 게이트웨이에 대 한 설명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b203-108">The **Set-AzureRmDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="7b203-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7b203-109">EXAMPLES</span></span>

### <span data-ttu-id="7b203-110">예제 1: 게이트웨이에 대 한 설명 설정</span><span class="sxs-lookup"><span data-stu-id="7b203-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
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

<span data-ttu-id="7b203-111">이 명령은 WikiADF 이라는 data factory의 ContosoGateway 이라는 게이트웨이에 대 한 설명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b203-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="7b203-112">Description 매개 변수는 새 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b203-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="7b203-113">변수</span><span class="sxs-lookup"><span data-stu-id="7b203-113">PARAMETERS</span></span>

### <span data-ttu-id="7b203-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7b203-114">-DataFactory</span></span>
<span data-ttu-id="7b203-115">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b203-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="7b203-116">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 게이트웨이에 대 한 설명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b203-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7b203-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7b203-117">-DataFactoryName</span></span>
<span data-ttu-id="7b203-118">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b203-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7b203-119">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리의 게이트웨이에 대 한 설명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b203-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7b203-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b203-120">-DefaultProfile</span></span>
<span data-ttu-id="7b203-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7b203-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b203-122">-설명</span><span class="sxs-lookup"><span data-stu-id="7b203-122">-Description</span></span>
<span data-ttu-id="7b203-123">게이트웨이에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b203-123">Specifies a description for the gateway.</span></span>

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

### <span data-ttu-id="7b203-124">-이름</span><span class="sxs-lookup"><span data-stu-id="7b203-124">-Name</span></span>
<span data-ttu-id="7b203-125">설명을 설정할 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b203-125">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="7b203-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b203-126">-ResourceGroupName</span></span>
<span data-ttu-id="7b203-127">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b203-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7b203-128">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 게이트웨이에 대 한 설명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b203-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7b203-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b203-129">CommonParameters</span></span>
<span data-ttu-id="7b203-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b203-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b203-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b203-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b203-132">입력</span><span class="sxs-lookup"><span data-stu-id="7b203-132">INPUTS</span></span>

### <span data-ttu-id="7b203-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7b203-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="7b203-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7b203-134">System.String</span></span>

## <span data-ttu-id="7b203-135">출력</span><span class="sxs-lookup"><span data-stu-id="7b203-135">OUTPUTS</span></span>

### <span data-ttu-id="7b203-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="7b203-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="7b203-137">상속자</span><span class="sxs-lookup"><span data-stu-id="7b203-137">NOTES</span></span>
* <span data-ttu-id="7b203-138">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="7b203-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7b203-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b203-139">RELATED LINKS</span></span>

[<span data-ttu-id="7b203-140">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="7b203-140">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="7b203-141">새로운 AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="7b203-141">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="7b203-142">제거-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="7b203-142">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)


