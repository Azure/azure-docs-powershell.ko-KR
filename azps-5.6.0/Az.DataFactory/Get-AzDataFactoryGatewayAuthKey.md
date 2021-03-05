---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 7987f014b08250975a2a25323122a081d508b036
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975435"
---
# <span data-ttu-id="933d4-101">Get-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="933d4-101">Get-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="933d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="933d4-102">SYNOPSIS</span></span>
<span data-ttu-id="933d4-103">Azure Data Factory에 대한 게이트웨이 Auth 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="933d4-103">Gets gateway auth key for an Azure Data Factory.</span></span>

## <span data-ttu-id="933d4-104">구문</span><span class="sxs-lookup"><span data-stu-id="933d4-104">SYNTAX</span></span>

### <span data-ttu-id="933d4-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="933d4-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="933d4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="933d4-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="933d4-107">설명</span><span class="sxs-lookup"><span data-stu-id="933d4-107">DESCRIPTION</span></span>
<span data-ttu-id="933d4-108">**Get-AzDataFactoryGatewayAuthKey** cmdlet은 지정된 Azure Data Factory 게이트웨이에 대한 게이트웨이 Auth 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="933d4-108">The **Get-AzDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="933d4-109">이 공개 키의 키1 또는 key2를 사용하여 클라우드 서비스에 게이트웨이를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="933d4-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="933d4-110">예제</span><span class="sxs-lookup"><span data-stu-id="933d4-110">EXAMPLES</span></span>

### <span data-ttu-id="933d4-111">예제 1: 게이트웨이의 auth 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="933d4-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="933d4-112">이 명령은 MyGateway라는 데이터 팩터리 게이트웨이에 대한 게이트웨이 auth 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="933d4-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="933d4-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="933d4-113">PARAMETERS</span></span>

### <span data-ttu-id="933d4-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="933d4-114">-DataFactoryName</span></span>
<span data-ttu-id="933d4-115">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="933d4-115">The data factory name.</span></span>

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

### <span data-ttu-id="933d4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="933d4-116">-DefaultProfile</span></span>
<span data-ttu-id="933d4-117">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="933d4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="933d4-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="933d4-118">-GatewayName</span></span>
<span data-ttu-id="933d4-119">데이터 팩터리 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="933d4-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="933d4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="933d4-120">-InputObject</span></span>
<span data-ttu-id="933d4-121">데이터 팩터리 개체</span><span class="sxs-lookup"><span data-stu-id="933d4-121">The data factory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="933d4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="933d4-122">-ResourceGroupName</span></span>
<span data-ttu-id="933d4-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="933d4-123">The resource group name.</span></span>

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

### <span data-ttu-id="933d4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="933d4-124">CommonParameters</span></span>
<span data-ttu-id="933d4-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="933d4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="933d4-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="933d4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="933d4-127">입력</span><span class="sxs-lookup"><span data-stu-id="933d4-127">INPUTS</span></span>

### <span data-ttu-id="933d4-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="933d4-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="933d4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="933d4-129">System.String</span></span>

## <span data-ttu-id="933d4-130">출력</span><span class="sxs-lookup"><span data-stu-id="933d4-130">OUTPUTS</span></span>

### <span data-ttu-id="933d4-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="933d4-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="933d4-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="933d4-132">NOTES</span></span>
* <span data-ttu-id="933d4-133">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="933d4-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="933d4-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="933d4-134">RELATED LINKS</span></span>

<span data-ttu-id="933d4-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="933d4-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span></span>

