---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
ms.openlocfilehash: 91a61935552258e5ca52ded6e05729deecaf5665
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495298"
---
# <span data-ttu-id="304a9-101">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="304a9-101">Get-AzIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="304a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="304a9-102">SYNOPSIS</span></span>
<span data-ttu-id="304a9-103">통합 계정 콜백 URL을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="304a9-103">Gets an integration account callback URL.</span></span>

## <span data-ttu-id="304a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="304a9-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="304a9-105">설명</span><span class="sxs-lookup"><span data-stu-id="304a9-105">DESCRIPTION</span></span>
<span data-ttu-id="304a9-106">**Get-AzIntegrationAccountCallbackUrl** cmdlet은 리소스 그룹에서 통합 계정 콜백 URL을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="304a9-106">The **Get-AzIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="304a9-107">이 cmdlet은 통합 계정 콜백 URL을 나타내는 **CallbackUrl** 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="304a9-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="304a9-108">통합 계정 이름 및 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="304a9-108">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="304a9-109">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="304a9-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="304a9-110">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="304a9-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="304a9-111">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="304a9-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="304a9-112">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="304a9-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="304a9-113">예제</span><span class="sxs-lookup"><span data-stu-id="304a9-113">EXAMPLES</span></span>

### <span data-ttu-id="304a9-114">예제 1: 통합 계정 콜백 URL 다운로드</span><span class="sxs-lookup"><span data-stu-id="304a9-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="304a9-115">이 명령은 통합 계정 콜백 URL을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="304a9-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="304a9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="304a9-116">PARAMETERS</span></span>

### <span data-ttu-id="304a9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="304a9-117">-DefaultProfile</span></span>
<span data-ttu-id="304a9-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="304a9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="304a9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="304a9-119">-Name</span></span>
<span data-ttu-id="304a9-120">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="304a9-120">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="304a9-121">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="304a9-121">-NotAfter</span></span>
<span data-ttu-id="304a9-122">콜백 URL의 만료 날짜를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="304a9-122">Specifies the expiry date for the callback URL.</span></span>

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

### <span data-ttu-id="304a9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="304a9-123">-ResourceGroupName</span></span>
<span data-ttu-id="304a9-124">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="304a9-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="304a9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="304a9-125">CommonParameters</span></span>
<span data-ttu-id="304a9-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="304a9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="304a9-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="304a9-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="304a9-128">입력</span><span class="sxs-lookup"><span data-stu-id="304a9-128">INPUTS</span></span>

### <span data-ttu-id="304a9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="304a9-129">System.String</span></span>

## <span data-ttu-id="304a9-130">출력</span><span class="sxs-lookup"><span data-stu-id="304a9-130">OUTPUTS</span></span>

### <span data-ttu-id="304a9-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="304a9-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="304a9-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="304a9-132">NOTES</span></span>

## <span data-ttu-id="304a9-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="304a9-133">RELATED LINKS</span></span>

[<span data-ttu-id="304a9-134">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="304a9-134">Get-AzLogicAppTriggerCallbackUrl</span></span>](./Get-AzLogicAppTriggerCallbackUrl.md)


