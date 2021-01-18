---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 46927e25fb4e32aae9ea1870ef9eeaedd5efe008
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495295"
---
# <span data-ttu-id="29ee7-101">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="29ee7-101">Get-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="29ee7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29ee7-102">SYNOPSIS</span></span>
<span data-ttu-id="29ee7-103">리소스 그룹에서 통합 계정 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="29ee7-103">Gets integration account certificates from a resource group.</span></span>

## <span data-ttu-id="29ee7-104">구문</span><span class="sxs-lookup"><span data-stu-id="29ee7-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>] [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29ee7-105">설명</span><span class="sxs-lookup"><span data-stu-id="29ee7-105">DESCRIPTION</span></span>
<span data-ttu-id="29ee7-106">**Get-AzIntegrationAccountCertificate** cmdlet은 리소스 그룹에서 통합 계정 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="29ee7-106">The **Get-AzIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="29ee7-107">통합 계정 이름, 리소스 그룹 이름 및 인증서 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29ee7-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="29ee7-108">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="29ee7-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="29ee7-109">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="29ee7-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="29ee7-110">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="29ee7-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="29ee7-111">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="29ee7-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="29ee7-112">예제</span><span class="sxs-lookup"><span data-stu-id="29ee7-112">EXAMPLES</span></span>

### <span data-ttu-id="29ee7-113">예제 1: 통합 계정 인증서를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29ee7-113">Example 1: Get an integration account certificate</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="29ee7-114">이 명령은 IntegrationAccountCertificate01이라는 통합 계정 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="29ee7-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="29ee7-115">예제 2: 통합 계정 이름으로 통합 계정 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="29ee7-115">Example 2: Get integration account certificates by integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="29ee7-116">이 명령은 IntegrationAccount31이라는 통합 계정에 대한 통합 계정 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="29ee7-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="29ee7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29ee7-117">PARAMETERS</span></span>

### <span data-ttu-id="29ee7-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="29ee7-118">-CertificateName</span></span>
<span data-ttu-id="29ee7-119">통합 계정 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29ee7-119">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="29ee7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29ee7-120">-DefaultProfile</span></span>
<span data-ttu-id="29ee7-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="29ee7-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29ee7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="29ee7-122">-Name</span></span>
<span data-ttu-id="29ee7-123">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29ee7-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="29ee7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29ee7-124">-ResourceGroupName</span></span>
<span data-ttu-id="29ee7-125">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29ee7-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="29ee7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29ee7-126">CommonParameters</span></span>
<span data-ttu-id="29ee7-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="29ee7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29ee7-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="29ee7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29ee7-129">입력</span><span class="sxs-lookup"><span data-stu-id="29ee7-129">INPUTS</span></span>

### <span data-ttu-id="29ee7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="29ee7-130">System.String</span></span>

## <span data-ttu-id="29ee7-131">출력</span><span class="sxs-lookup"><span data-stu-id="29ee7-131">OUTPUTS</span></span>

### <span data-ttu-id="29ee7-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="29ee7-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="29ee7-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="29ee7-133">NOTES</span></span>

## <span data-ttu-id="29ee7-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29ee7-134">RELATED LINKS</span></span>

[<span data-ttu-id="29ee7-135">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="29ee7-135">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="29ee7-136">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="29ee7-136">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="29ee7-137">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="29ee7-137">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


