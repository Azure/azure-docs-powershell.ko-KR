---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
ms.openlocfilehash: e4046424a1388941af967782f9778177bcfbbb1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867762"
---
# <span data-ttu-id="fecd5-101">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="fecd5-101">Get-AzIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="fecd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fecd5-102">SYNOPSIS</span></span>
<span data-ttu-id="fecd5-103">통합 계정 콜백 URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fecd5-103">Gets an integration account callback URL.</span></span>

## <span data-ttu-id="fecd5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fecd5-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fecd5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fecd5-105">DESCRIPTION</span></span>
<span data-ttu-id="fecd5-106">**Get-AzIntegrationAccountCallbackUrl** cmdlet은 리소스 그룹에서 통합 계정 콜백 URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fecd5-106">The **Get-AzIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="fecd5-107">이 cmdlet은 통합 계정 콜백 URL을 나타내는 **callbackurl** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fecd5-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="fecd5-108">통합 계정 이름 및 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fecd5-108">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="fecd5-109">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fecd5-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="fecd5-110">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="fecd5-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="fecd5-111">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fecd5-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="fecd5-112">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fecd5-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="fecd5-113">예제의</span><span class="sxs-lookup"><span data-stu-id="fecd5-113">EXAMPLES</span></span>

### <span data-ttu-id="fecd5-114">예제 1: 통합 계정 콜백 URL 가져오기</span><span class="sxs-lookup"><span data-stu-id="fecd5-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="fecd5-115">이 명령은 통합 계정 콜백 URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fecd5-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="fecd5-116">변수</span><span class="sxs-lookup"><span data-stu-id="fecd5-116">PARAMETERS</span></span>

### <span data-ttu-id="fecd5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fecd5-117">-DefaultProfile</span></span>
<span data-ttu-id="fecd5-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fecd5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fecd5-119">-이름</span><span class="sxs-lookup"><span data-stu-id="fecd5-119">-Name</span></span>
<span data-ttu-id="fecd5-120">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fecd5-120">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fecd5-121">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="fecd5-121">-NotAfter</span></span>
<span data-ttu-id="fecd5-122">콜백 URL에 대 한 만료 날짜를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fecd5-122">Specifies the expiry date for the callback URL.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fecd5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fecd5-123">-ResourceGroupName</span></span>
<span data-ttu-id="fecd5-124">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fecd5-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fecd5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fecd5-125">CommonParameters</span></span>
<span data-ttu-id="fecd5-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fecd5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fecd5-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fecd5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fecd5-128">입력</span><span class="sxs-lookup"><span data-stu-id="fecd5-128">INPUTS</span></span>

### <span data-ttu-id="fecd5-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fecd5-129">System.String</span></span>

## <span data-ttu-id="fecd5-130">출력</span><span class="sxs-lookup"><span data-stu-id="fecd5-130">OUTPUTS</span></span>

### <span data-ttu-id="fecd5-131">Microsoft. 관리자. CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="fecd5-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="fecd5-132">상속자</span><span class="sxs-lookup"><span data-stu-id="fecd5-132">NOTES</span></span>

## <span data-ttu-id="fecd5-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fecd5-133">RELATED LINKS</span></span>

[<span data-ttu-id="fecd5-134">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="fecd5-134">Get-AzLogicAppTriggerCallbackUrl</span></span>](./Get-AzLogicAppTriggerCallbackUrl.md)


