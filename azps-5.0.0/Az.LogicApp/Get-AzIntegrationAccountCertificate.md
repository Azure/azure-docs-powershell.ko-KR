---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 46927e25fb4e32aae9ea1870ef9eeaedd5efe008
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226889"
---
# <span data-ttu-id="10fde-101">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="10fde-101">Get-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="10fde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10fde-102">SYNOPSIS</span></span>
<span data-ttu-id="10fde-103">리소스 그룹에서 통합 계정 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="10fde-103">Gets integration account certificates from a resource group.</span></span>

## <span data-ttu-id="10fde-104">구문과</span><span class="sxs-lookup"><span data-stu-id="10fde-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>] [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10fde-105">설명은</span><span class="sxs-lookup"><span data-stu-id="10fde-105">DESCRIPTION</span></span>
<span data-ttu-id="10fde-106">**Get-AzIntegrationAccountCertificate** cmdlet은 리소스 그룹에서 통합 계정 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="10fde-106">The **Get-AzIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="10fde-107">통합 계정 이름, 리소스 그룹 이름 및 인증서 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10fde-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="10fde-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="10fde-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="10fde-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="10fde-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="10fde-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="10fde-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="10fde-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="10fde-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="10fde-112">예제의</span><span class="sxs-lookup"><span data-stu-id="10fde-112">EXAMPLES</span></span>

### <span data-ttu-id="10fde-113">예제 1: 통합 계정 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="10fde-113">Example 1: Get an integration account certificate</span></span>
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

<span data-ttu-id="10fde-114">이 명령은 IntegrationAccountCertificate01 이라는 통합 계정 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="10fde-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="10fde-115">예제 2: 통합 계정 이름을 기준으로 통합 계정 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="10fde-115">Example 2: Get integration account certificates by integration account name</span></span>
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

<span data-ttu-id="10fde-116">이 명령은 IntegrationAccount31 이라는 통합 계정에 대 한 통합 계정 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="10fde-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="10fde-117">변수</span><span class="sxs-lookup"><span data-stu-id="10fde-117">PARAMETERS</span></span>

### <span data-ttu-id="10fde-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="10fde-118">-CertificateName</span></span>
<span data-ttu-id="10fde-119">통합 계정 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10fde-119">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="10fde-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10fde-120">-DefaultProfile</span></span>
<span data-ttu-id="10fde-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="10fde-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10fde-122">-이름</span><span class="sxs-lookup"><span data-stu-id="10fde-122">-Name</span></span>
<span data-ttu-id="10fde-123">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10fde-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="10fde-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10fde-124">-ResourceGroupName</span></span>
<span data-ttu-id="10fde-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10fde-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="10fde-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10fde-126">CommonParameters</span></span>
<span data-ttu-id="10fde-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="10fde-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10fde-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10fde-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10fde-129">입력</span><span class="sxs-lookup"><span data-stu-id="10fde-129">INPUTS</span></span>

### <span data-ttu-id="10fde-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="10fde-130">System.String</span></span>

## <span data-ttu-id="10fde-131">출력</span><span class="sxs-lookup"><span data-stu-id="10fde-131">OUTPUTS</span></span>

### <span data-ttu-id="10fde-132">IntegrationAccountCertificate를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="10fde-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="10fde-133">상속자</span><span class="sxs-lookup"><span data-stu-id="10fde-133">NOTES</span></span>

## <span data-ttu-id="10fde-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10fde-134">RELATED LINKS</span></span>

[<span data-ttu-id="10fde-135">새로운 AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="10fde-135">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="10fde-136">제거-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="10fde-136">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="10fde-137">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="10fde-137">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


