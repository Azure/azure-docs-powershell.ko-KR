---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCallbackUrl.md
ms.openlocfilehash: 6cbb37eb211c766959f2513abe3bbe1554bfdb23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527519"
---
# <span data-ttu-id="743ae-101">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="743ae-101">Get-AzureRmIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="743ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="743ae-102">SYNOPSIS</span></span>
<span data-ttu-id="743ae-103">통합 계정 콜백 URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="743ae-103">Gets an integration account callback URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="743ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="743ae-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="743ae-105">설명은</span><span class="sxs-lookup"><span data-stu-id="743ae-105">DESCRIPTION</span></span>
<span data-ttu-id="743ae-106">**Get-AzureRmIntegrationAccountCallbackUrl** cmdlet은 리소스 그룹에서 통합 계정 콜백 URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="743ae-106">The **Get-AzureRmIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="743ae-107">이 cmdlet은 통합 계정 콜백 URL을 나타내는 **callbackurl** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="743ae-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="743ae-108">통합 계정 이름 및 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="743ae-108">Specify the integration account name and resource group name.</span></span>

<span data-ttu-id="743ae-109">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="743ae-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="743ae-110">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="743ae-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="743ae-111">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="743ae-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="743ae-112">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="743ae-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="743ae-113">예제의</span><span class="sxs-lookup"><span data-stu-id="743ae-113">EXAMPLES</span></span>

### <span data-ttu-id="743ae-114">예제 1: 통합 계정 콜백 URL 가져오기</span><span class="sxs-lookup"><span data-stu-id="743ae-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="743ae-115">이 명령은 통합 계정 콜백 URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="743ae-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="743ae-116">변수</span><span class="sxs-lookup"><span data-stu-id="743ae-116">PARAMETERS</span></span>

### <span data-ttu-id="743ae-117">-이름</span><span class="sxs-lookup"><span data-stu-id="743ae-117">-Name</span></span>
<span data-ttu-id="743ae-118">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="743ae-118">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="743ae-119">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="743ae-119">-NotAfter</span></span>
<span data-ttu-id="743ae-120">콜백 URL에 대 한 만료 날짜를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="743ae-120">Specifies the expiry date for the callback URL.</span></span>

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

### <span data-ttu-id="743ae-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="743ae-121">-ResourceGroupName</span></span>
<span data-ttu-id="743ae-122">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="743ae-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="743ae-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="743ae-123">-DefaultProfile</span></span>
<span data-ttu-id="743ae-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="743ae-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="743ae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="743ae-125">CommonParameters</span></span>
<span data-ttu-id="743ae-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="743ae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="743ae-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="743ae-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="743ae-128">입력</span><span class="sxs-lookup"><span data-stu-id="743ae-128">INPUTS</span></span>

## <span data-ttu-id="743ae-129">출력</span><span class="sxs-lookup"><span data-stu-id="743ae-129">OUTPUTS</span></span>

### <span data-ttu-id="743ae-130">Microsoft. 관리자. CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="743ae-130">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="743ae-131">상속자</span><span class="sxs-lookup"><span data-stu-id="743ae-131">NOTES</span></span>

## <span data-ttu-id="743ae-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="743ae-132">RELATED LINKS</span></span>

[<span data-ttu-id="743ae-133">Get-AzureRmLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="743ae-133">Get-AzureRmLogicAppTriggerCallbackUrl</span></span>](./Get-AzureRmLogicAppTriggerCallbackUrl.md)


