---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: ed1cbf5fb39ba89427260225ecad0b4b8b5b1461
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697083"
---
# <span data-ttu-id="75019-101">Get-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="75019-101">Get-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="75019-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75019-102">SYNOPSIS</span></span>
<span data-ttu-id="75019-103">Azure Data Factory에 대 한 게이트웨이 인증 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75019-103">Gets gateway auth key for an Azure Data Factory.</span></span>

## <span data-ttu-id="75019-104">구문과</span><span class="sxs-lookup"><span data-stu-id="75019-104">SYNTAX</span></span>

### <span data-ttu-id="75019-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="75019-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75019-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="75019-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75019-107">설명은</span><span class="sxs-lookup"><span data-stu-id="75019-107">DESCRIPTION</span></span>
<span data-ttu-id="75019-108">**AzDataFactoryGatewayAuthKey** cmdlet은 지정 된 Azure Data Factory 게이트웨이에 대 한 게이트웨이 인증 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75019-108">The **Get-AzDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="75019-109">이 auth 키의 key1 또는 key2를 사용 하 여 클라우드 서비스에 게이트웨이를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="75019-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="75019-110">예제의</span><span class="sxs-lookup"><span data-stu-id="75019-110">EXAMPLES</span></span>

### <span data-ttu-id="75019-111">예제 1: 게이트웨이의 auth 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75019-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="75019-112">이 명령은 MyGateway 라는 data factory gateway에 대 한 게이트웨이 인증 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75019-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="75019-113">변수</span><span class="sxs-lookup"><span data-stu-id="75019-113">PARAMETERS</span></span>

### <span data-ttu-id="75019-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="75019-114">-DataFactoryName</span></span>
<span data-ttu-id="75019-115">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75019-115">The data factory name.</span></span>

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

### <span data-ttu-id="75019-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75019-116">-DefaultProfile</span></span>
<span data-ttu-id="75019-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="75019-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75019-118">--게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="75019-118">-GatewayName</span></span>
<span data-ttu-id="75019-119">Data factory 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75019-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="75019-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75019-120">-InputObject</span></span>
<span data-ttu-id="75019-121">Data factory 개체</span><span class="sxs-lookup"><span data-stu-id="75019-121">The data factory object</span></span>

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

### <span data-ttu-id="75019-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75019-122">-ResourceGroupName</span></span>
<span data-ttu-id="75019-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75019-123">The resource group name.</span></span>

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

### <span data-ttu-id="75019-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75019-124">CommonParameters</span></span>
<span data-ttu-id="75019-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75019-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75019-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75019-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75019-127">입력</span><span class="sxs-lookup"><span data-stu-id="75019-127">INPUTS</span></span>

### <span data-ttu-id="75019-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="75019-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="75019-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="75019-129">System.String</span></span>

## <span data-ttu-id="75019-130">출력</span><span class="sxs-lookup"><span data-stu-id="75019-130">OUTPUTS</span></span>

### <span data-ttu-id="75019-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="75019-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="75019-132">상속자</span><span class="sxs-lookup"><span data-stu-id="75019-132">NOTES</span></span>
* <span data-ttu-id="75019-133">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="75019-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="75019-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75019-134">RELATED LINKS</span></span>

<span data-ttu-id="75019-135">[새로운 AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [새로운 AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="75019-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span></span>

