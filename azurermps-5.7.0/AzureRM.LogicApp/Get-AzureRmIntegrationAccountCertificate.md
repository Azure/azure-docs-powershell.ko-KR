---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 268dd2c54d9881281a5b1ee331a5b5d98892f7b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532792"
---
# <span data-ttu-id="a3ad2-101">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="a3ad2-101">Get-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="a3ad2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3ad2-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ad2-103">리소스 그룹에서 통합 계정 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3ad2-103">Gets integration account certificates from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3ad2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a3ad2-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>]
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3ad2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a3ad2-105">DESCRIPTION</span></span>
<span data-ttu-id="a3ad2-106">**Get-AzureRmIntegrationAccountCertificate** cmdlet은 리소스 그룹에서 통합 계정 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3ad2-106">The **Get-AzureRmIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="a3ad2-107">통합 계정 이름, 리소스 그룹 이름 및 인증서 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3ad2-107">Specify the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="a3ad2-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3ad2-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a3ad2-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3ad2-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a3ad2-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3ad2-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a3ad2-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3ad2-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a3ad2-112">예제의</span><span class="sxs-lookup"><span data-stu-id="a3ad2-112">EXAMPLES</span></span>

### <span data-ttu-id="a3ad2-113">예제 1: 통합 계정 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="a3ad2-113">Example 1: Get an integration account certificate</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="a3ad2-114">이 명령은 IntegrationAccountCertificate01 이라는 통합 계정 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3ad2-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="a3ad2-115">예제 2: 통합 계정 이름을 기준으로 통합 계정 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="a3ad2-115">Example 2: Get integration account certificates by integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="a3ad2-116">이 명령은 IntegrationAccount31 이라는 통합 계정에 대 한 통합 계정 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3ad2-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="a3ad2-117">변수</span><span class="sxs-lookup"><span data-stu-id="a3ad2-117">PARAMETERS</span></span>

### <span data-ttu-id="a3ad2-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="a3ad2-118">-CertificateName</span></span>
<span data-ttu-id="a3ad2-119">통합 계정 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3ad2-119">Specifies the name of an integration account certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ad2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ad2-120">-DefaultProfile</span></span>
<span data-ttu-id="a3ad2-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a3ad2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ad2-122">-이름</span><span class="sxs-lookup"><span data-stu-id="a3ad2-122">-Name</span></span>
<span data-ttu-id="a3ad2-123">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3ad2-123">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ad2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3ad2-124">-ResourceGroupName</span></span>
<span data-ttu-id="a3ad2-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3ad2-125">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3ad2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ad2-126">CommonParameters</span></span>
<span data-ttu-id="a3ad2-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3ad2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ad2-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3ad2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ad2-129">입력</span><span class="sxs-lookup"><span data-stu-id="a3ad2-129">INPUTS</span></span>

### <span data-ttu-id="a3ad2-130">않아야</span><span class="sxs-lookup"><span data-stu-id="a3ad2-130">None</span></span>
<span data-ttu-id="a3ad2-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3ad2-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a3ad2-132">출력</span><span class="sxs-lookup"><span data-stu-id="a3ad2-132">OUTPUTS</span></span>

### <span data-ttu-id="a3ad2-133">IntegrationAccountCertificate를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="a3ad2-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="a3ad2-134">상속자</span><span class="sxs-lookup"><span data-stu-id="a3ad2-134">NOTES</span></span>

## <span data-ttu-id="a3ad2-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3ad2-135">RELATED LINKS</span></span>

[<span data-ttu-id="a3ad2-136">새로운 AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="a3ad2-136">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="a3ad2-137">제거-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="a3ad2-137">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="a3ad2-138">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="a3ad2-138">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


