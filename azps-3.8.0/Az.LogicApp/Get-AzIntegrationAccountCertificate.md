---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 46927e25fb4e32aae9ea1870ef9eeaedd5efe008
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878234"
---
# <span data-ttu-id="9ec97-101">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9ec97-101">Get-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="9ec97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ec97-102">SYNOPSIS</span></span>
<span data-ttu-id="9ec97-103">리소스 그룹에서 통합 계정 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ec97-103">Gets integration account certificates from a resource group.</span></span>

## <span data-ttu-id="9ec97-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ec97-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>] [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ec97-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9ec97-105">DESCRIPTION</span></span>
<span data-ttu-id="9ec97-106">**Get-AzIntegrationAccountCertificate** cmdlet은 리소스 그룹에서 통합 계정 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ec97-106">The **Get-AzIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="9ec97-107">통합 계정 이름, 리소스 그룹 이름 및 인증서 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ec97-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="9ec97-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ec97-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9ec97-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ec97-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9ec97-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ec97-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9ec97-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ec97-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9ec97-112">예제의</span><span class="sxs-lookup"><span data-stu-id="9ec97-112">EXAMPLES</span></span>

### <span data-ttu-id="9ec97-113">예제 1: 통합 계정 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="9ec97-113">Example 1: Get an integration account certificate</span></span>
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

<span data-ttu-id="9ec97-114">이 명령은 IntegrationAccountCertificate01 이라는 통합 계정 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ec97-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="9ec97-115">예제 2: 통합 계정 이름을 기준으로 통합 계정 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="9ec97-115">Example 2: Get integration account certificates by integration account name</span></span>
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

<span data-ttu-id="9ec97-116">이 명령은 IntegrationAccount31 이라는 통합 계정에 대 한 통합 계정 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ec97-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="9ec97-117">변수</span><span class="sxs-lookup"><span data-stu-id="9ec97-117">PARAMETERS</span></span>

### <span data-ttu-id="9ec97-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="9ec97-118">-CertificateName</span></span>
<span data-ttu-id="9ec97-119">통합 계정 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ec97-119">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="9ec97-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ec97-120">-DefaultProfile</span></span>
<span data-ttu-id="9ec97-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9ec97-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ec97-122">-이름</span><span class="sxs-lookup"><span data-stu-id="9ec97-122">-Name</span></span>
<span data-ttu-id="9ec97-123">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ec97-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="9ec97-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ec97-124">-ResourceGroupName</span></span>
<span data-ttu-id="9ec97-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ec97-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9ec97-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ec97-126">CommonParameters</span></span>
<span data-ttu-id="9ec97-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ec97-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ec97-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ec97-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ec97-129">입력</span><span class="sxs-lookup"><span data-stu-id="9ec97-129">INPUTS</span></span>

### <span data-ttu-id="9ec97-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9ec97-130">System.String</span></span>

## <span data-ttu-id="9ec97-131">출력</span><span class="sxs-lookup"><span data-stu-id="9ec97-131">OUTPUTS</span></span>

### <span data-ttu-id="9ec97-132">IntegrationAccountCertificate를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="9ec97-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="9ec97-133">상속자</span><span class="sxs-lookup"><span data-stu-id="9ec97-133">NOTES</span></span>

## <span data-ttu-id="9ec97-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ec97-134">RELATED LINKS</span></span>

[<span data-ttu-id="9ec97-135">새로운 AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9ec97-135">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="9ec97-136">제거-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9ec97-136">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="9ec97-137">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9ec97-137">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


