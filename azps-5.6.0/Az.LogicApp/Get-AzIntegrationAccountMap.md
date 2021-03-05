---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
ms.openlocfilehash: ef13fd50877076fb11382623b5e7950098204997
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960603"
---
# <span data-ttu-id="17fa7-101">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="17fa7-101">Get-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="17fa7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17fa7-102">SYNOPSIS</span></span>
<span data-ttu-id="17fa7-103">통합 계정 맵을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="17fa7-103">Gets an integration account map.</span></span>

## <span data-ttu-id="17fa7-104">구문</span><span class="sxs-lookup"><span data-stu-id="17fa7-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-MapType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17fa7-105">설명</span><span class="sxs-lookup"><span data-stu-id="17fa7-105">DESCRIPTION</span></span>
<span data-ttu-id="17fa7-106">**Get-AzIntegrationAccountMap** cmdlet은 리소스 그룹에서 통합 계정 맵을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="17fa7-106">The **Get-AzIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="17fa7-107">통합 계정 이름, 리소스 그룹 이름 및 맵 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="17fa7-107">Specifying the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="17fa7-108">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="17fa7-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="17fa7-109">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="17fa7-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="17fa7-110">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 뒤 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="17fa7-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="17fa7-111">필요한 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="17fa7-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="17fa7-112">예제</span><span class="sxs-lookup"><span data-stu-id="17fa7-112">EXAMPLES</span></span>

### <span data-ttu-id="17fa7-113">예제 1: 통합 계정 맵 보기</span><span class="sxs-lookup"><span data-stu-id="17fa7-113">Example 1: Get an integration account map</span></span>
```
PS C:\>Get-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="17fa7-114">이 명령은 지정된 리소스 그룹에서 IntegrationAccountMap47이라는 통합 계정 맵을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="17fa7-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="17fa7-115">예제 2: 통합 계정 이름으로 통합 계정 맵 다운로드</span><span class="sxs-lookup"><span data-stu-id="17fa7-115">Example 2: Get integration account maps by integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="17fa7-116">이 명령은 통합 계정 이름에 의해 통합 계정 맵을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="17fa7-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="17fa7-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="17fa7-117">PARAMETERS</span></span>

### <span data-ttu-id="17fa7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17fa7-118">-DefaultProfile</span></span>
<span data-ttu-id="17fa7-119">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="17fa7-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17fa7-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="17fa7-120">-MapName</span></span>
<span data-ttu-id="17fa7-121">통합 계정 맵의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="17fa7-121">Specifies the name of an integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17fa7-122">-MapType</span><span class="sxs-lookup"><span data-stu-id="17fa7-122">-MapType</span></span>
<span data-ttu-id="17fa7-123">통합 계정 맵 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="17fa7-123">The integration account map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17fa7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="17fa7-124">-Name</span></span>
<span data-ttu-id="17fa7-125">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="17fa7-125">Specifies the name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17fa7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17fa7-126">-ResourceGroupName</span></span>
<span data-ttu-id="17fa7-127">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="17fa7-127">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17fa7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17fa7-128">CommonParameters</span></span>
<span data-ttu-id="17fa7-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="17fa7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17fa7-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="17fa7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17fa7-131">입력</span><span class="sxs-lookup"><span data-stu-id="17fa7-131">INPUTS</span></span>

### <span data-ttu-id="17fa7-132">System.String</span><span class="sxs-lookup"><span data-stu-id="17fa7-132">System.String</span></span>

## <span data-ttu-id="17fa7-133">출력</span><span class="sxs-lookup"><span data-stu-id="17fa7-133">OUTPUTS</span></span>

### <span data-ttu-id="17fa7-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="17fa7-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="17fa7-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="17fa7-135">NOTES</span></span>

## <span data-ttu-id="17fa7-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17fa7-136">RELATED LINKS</span></span>

[<span data-ttu-id="17fa7-137">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="17fa7-137">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="17fa7-138">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="17fa7-138">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="17fa7-139">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="17fa7-139">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


