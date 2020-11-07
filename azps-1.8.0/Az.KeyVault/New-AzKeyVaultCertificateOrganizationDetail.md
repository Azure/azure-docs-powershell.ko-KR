---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateorganizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
ms.openlocfilehash: ac9313611e5c228d33ea2dd473b0669e54ab1ca1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867949"
---
# <span data-ttu-id="6a42b-101">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="6a42b-101">New-AzKeyVaultCertificateOrganizationDetail</span></span>

## <span data-ttu-id="6a42b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a42b-102">SYNOPSIS</span></span>
<span data-ttu-id="6a42b-103">메모리 내 인증서 조직 세부 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6a42b-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="6a42b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6a42b-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetail [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a42b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6a42b-105">DESCRIPTION</span></span>
<span data-ttu-id="6a42b-106">**AzKeyVaultCertificateOrganizationDetail** cmdlet은 메모리 내 인증서 조직 세부 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6a42b-106">The **New-AzKeyVaultCertificateOrganizationDetail** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="6a42b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6a42b-107">EXAMPLES</span></span>

### <span data-ttu-id="6a42b-108">예제 1: 조직 세부 정보 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="6a42b-108">Example 1: Create an organization details object</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails

Id AdministratorDetails
-- --------------------
   {Patti}
```

<span data-ttu-id="6a42b-109">첫 번째 명령은 인증서 관리자 세부 정보 개체를 만든 다음 $AdminDetails 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a42b-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>
<span data-ttu-id="6a42b-110">두 번째 명령은 인증서 조직 세부 정보 개체를 만든 다음 $OrgDetails 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a42b-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="6a42b-111">변수</span><span class="sxs-lookup"><span data-stu-id="6a42b-111">PARAMETERS</span></span>

### <span data-ttu-id="6a42b-112">-관리자 세부 정보</span><span class="sxs-lookup"><span data-stu-id="6a42b-112">-AdministratorDetails</span></span>
<span data-ttu-id="6a42b-113">인증서 조직 관리자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a42b-113">Specifies the certificate organization administrators.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a42b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a42b-114">-DefaultProfile</span></span>
<span data-ttu-id="6a42b-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6a42b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a42b-116">-Id</span><span class="sxs-lookup"><span data-stu-id="6a42b-116">-Id</span></span>
<span data-ttu-id="6a42b-117">조직의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a42b-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="6a42b-118">-확인</span><span class="sxs-lookup"><span data-stu-id="6a42b-118">-Confirm</span></span>
<span data-ttu-id="6a42b-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a42b-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a42b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a42b-120">-WhatIf</span></span>
<span data-ttu-id="6a42b-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6a42b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a42b-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a42b-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a42b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a42b-123">CommonParameters</span></span>
<span data-ttu-id="6a42b-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a42b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a42b-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a42b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a42b-126">입력</span><span class="sxs-lookup"><span data-stu-id="6a42b-126">INPUTS</span></span>

### <span data-ttu-id="6a42b-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6a42b-127">System.String</span></span>

### <span data-ttu-id="6a42b-128">System.webserver. List ' 1 [[Microsoft Azure. PSKeyVaultCertificateAdministratorDetails, Microsoft azure. e-t 볼트. \*. i = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6a42b-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6a42b-129">출력</span><span class="sxs-lookup"><span data-stu-id="6a42b-129">OUTPUTS</span></span>

### <span data-ttu-id="6a42b-130">Microsoft. KeyVault. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="6a42b-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="6a42b-131">상속자</span><span class="sxs-lookup"><span data-stu-id="6a42b-131">NOTES</span></span>

## <span data-ttu-id="6a42b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a42b-132">RELATED LINKS</span></span>

[<span data-ttu-id="6a42b-133">새로운 AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="6a42b-133">New-AzKeyVaultCertificateAdministratorDetail</span></span>](./New-AzKeyVaultCertificateAdministratorDetail.md)

