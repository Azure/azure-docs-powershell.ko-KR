---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
ms.openlocfilehash: ed85c1fea8bd338b3dd4f2a9e82ee5aac3f3b52b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495283"
---
# <span data-ttu-id="405a4-101">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="405a4-101">Get-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="405a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="405a4-102">SYNOPSIS</span></span>
<span data-ttu-id="405a4-103">통합 계정 스마마를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-103">Gets integration account schemas.</span></span>

## <span data-ttu-id="405a4-104">구문</span><span class="sxs-lookup"><span data-stu-id="405a4-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="405a4-105">설명</span><span class="sxs-lookup"><span data-stu-id="405a4-105">DESCRIPTION</span></span>
<span data-ttu-id="405a4-106">**Get-AzIntegrationAccountSchema** cmdlet은 통합 계정 스마마를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-106">The **Get-AzIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="405a4-107">통합 계정 이름, 리소스 그룹 이름 및 스마마 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="405a4-108">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="405a4-109">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="405a4-110">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="405a4-111">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="405a4-112">예제</span><span class="sxs-lookup"><span data-stu-id="405a4-112">EXAMPLES</span></span>

### <span data-ttu-id="405a4-113">예제 1: 통합 계정 스마마를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-113">Example 1: Get an integration account schema</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="405a4-114">이 명령은 IntegrationAccountSchema43이라는 통합 계정 스마마를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="405a4-115">예제 2: 리소스 그룹에 대한 통합 계정 스마마를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-115">Example 2: Get integration account schemas for a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="405a4-116">이 명령은 ResourceGroup11이라는 리소스 그룹에 대한 통합 계정 스마마를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="405a4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="405a4-117">PARAMETERS</span></span>

### <span data-ttu-id="405a4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="405a4-118">-DefaultProfile</span></span>
<span data-ttu-id="405a4-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="405a4-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="405a4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="405a4-120">-Name</span></span>
<span data-ttu-id="405a4-121">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="405a4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="405a4-122">-ResourceGroupName</span></span>
<span data-ttu-id="405a4-123">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="405a4-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="405a4-124">-SchemaName</span></span>
<span data-ttu-id="405a4-125">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="405a4-126">스마마의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="405a4-127">.</span><span class="sxs-lookup"><span data-stu-id="405a4-127">.</span></span>

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

### <span data-ttu-id="405a4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="405a4-128">CommonParameters</span></span>
<span data-ttu-id="405a4-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="405a4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="405a4-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="405a4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="405a4-131">입력</span><span class="sxs-lookup"><span data-stu-id="405a4-131">INPUTS</span></span>

### <span data-ttu-id="405a4-132">System.String</span><span class="sxs-lookup"><span data-stu-id="405a4-132">System.String</span></span>

## <span data-ttu-id="405a4-133">출력</span><span class="sxs-lookup"><span data-stu-id="405a4-133">OUTPUTS</span></span>

### <span data-ttu-id="405a4-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="405a4-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="405a4-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="405a4-135">NOTES</span></span>

## <span data-ttu-id="405a4-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="405a4-136">RELATED LINKS</span></span>

[<span data-ttu-id="405a4-137">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="405a4-137">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="405a4-138">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="405a4-138">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="405a4-139">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="405a4-139">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


