---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 8e86597292a9bcfef2163100d273d1e27daeb32a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354578"
---
# <span data-ttu-id="f660e-101">Get-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="f660e-101">Get-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="f660e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f660e-102">SYNOPSIS</span></span>
<span data-ttu-id="f660e-103">Azure Data Factory에 대한 게이트웨이 Auth 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f660e-103">Gets gateway auth key for an Azure Data Factory.</span></span>

## <span data-ttu-id="f660e-104">구문</span><span class="sxs-lookup"><span data-stu-id="f660e-104">SYNTAX</span></span>

### <span data-ttu-id="f660e-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="f660e-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f660e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f660e-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f660e-107">설명</span><span class="sxs-lookup"><span data-stu-id="f660e-107">DESCRIPTION</span></span>
<span data-ttu-id="f660e-108">**Get-AzDataFactoryGatewayAuthKey** cmdlet은 지정된 Azure Data Factory 게이트웨이에 대한 게이트웨이 auth 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f660e-108">The **Get-AzDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="f660e-109">이 Auth 키의 key1 또는 key2를 사용하여 클라우드 서비스에 게이트웨이를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="f660e-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="f660e-110">예제</span><span class="sxs-lookup"><span data-stu-id="f660e-110">EXAMPLES</span></span>

### <span data-ttu-id="f660e-111">예제 1: 게이트웨이의 Auth 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f660e-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="f660e-112">이 명령은 MyGateway라는 데이터 팩터리 게이트웨이에 대한 게이트웨이 Auth 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f660e-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="f660e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f660e-113">PARAMETERS</span></span>

### <span data-ttu-id="f660e-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f660e-114">-DataFactoryName</span></span>
<span data-ttu-id="f660e-115">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f660e-115">The data factory name.</span></span>

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

### <span data-ttu-id="f660e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f660e-116">-DefaultProfile</span></span>
<span data-ttu-id="f660e-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f660e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f660e-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="f660e-118">-GatewayName</span></span>
<span data-ttu-id="f660e-119">데이터 팩터리 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f660e-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="f660e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f660e-120">-InputObject</span></span>
<span data-ttu-id="f660e-121">데이터 팩터리 개체</span><span class="sxs-lookup"><span data-stu-id="f660e-121">The data factory object</span></span>

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

### <span data-ttu-id="f660e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f660e-122">-ResourceGroupName</span></span>
<span data-ttu-id="f660e-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f660e-123">The resource group name.</span></span>

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

### <span data-ttu-id="f660e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f660e-124">CommonParameters</span></span>
<span data-ttu-id="f660e-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f660e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f660e-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f660e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f660e-127">입력</span><span class="sxs-lookup"><span data-stu-id="f660e-127">INPUTS</span></span>

### <span data-ttu-id="f660e-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f660e-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="f660e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f660e-129">System.String</span></span>

## <span data-ttu-id="f660e-130">출력</span><span class="sxs-lookup"><span data-stu-id="f660e-130">OUTPUTS</span></span>

### <span data-ttu-id="f660e-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="f660e-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="f660e-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f660e-132">NOTES</span></span>
* <span data-ttu-id="f660e-133">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="f660e-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f660e-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f660e-134">RELATED LINKS</span></span>

<span data-ttu-id="f660e-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="f660e-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span></span>

