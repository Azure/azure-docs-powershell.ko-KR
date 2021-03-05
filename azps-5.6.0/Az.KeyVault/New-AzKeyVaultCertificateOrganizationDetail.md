---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultcertificateorganizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
ms.openlocfilehash: ee2be43882eb434d8bbc533e0d10722f63427a83
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001344"
---
# <span data-ttu-id="254d1-101">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="254d1-101">New-AzKeyVaultCertificateOrganizationDetail</span></span>

## <span data-ttu-id="254d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="254d1-102">SYNOPSIS</span></span>
<span data-ttu-id="254d1-103">메모리 내 인증서 조직 세부 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="254d1-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="254d1-104">구문</span><span class="sxs-lookup"><span data-stu-id="254d1-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetail [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="254d1-105">설명</span><span class="sxs-lookup"><span data-stu-id="254d1-105">DESCRIPTION</span></span>
<span data-ttu-id="254d1-106">**New-AzKeyVaultCertificateOrganizationDetail** cmdlet은 메모리 내 인증서 조직 세부 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="254d1-106">The **New-AzKeyVaultCertificateOrganizationDetail** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="254d1-107">예제</span><span class="sxs-lookup"><span data-stu-id="254d1-107">EXAMPLES</span></span>

### <span data-ttu-id="254d1-108">예제 1: 조직 세부 정보 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="254d1-108">Example 1: Create an organization details object</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails

Id AdministratorDetails
-- --------------------
   {Patti}
```

<span data-ttu-id="254d1-109">첫 번째 명령은 인증서 관리자 세부 정보를 개체를 만든 다음, 해당 개체를 $AdminDetails 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="254d1-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>
<span data-ttu-id="254d1-110">두 번째 명령은 인증서 조직 세부 정보를 개체를 만든 다음, 해당 개체를 $OrgDetails 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="254d1-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="254d1-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="254d1-111">PARAMETERS</span></span>

### <span data-ttu-id="254d1-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="254d1-112">-AdministratorDetails</span></span>
<span data-ttu-id="254d1-113">인증서 조직 관리자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="254d1-113">Specifies the certificate organization administrators.</span></span>

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

### <span data-ttu-id="254d1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="254d1-114">-DefaultProfile</span></span>
<span data-ttu-id="254d1-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="254d1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="254d1-116">-Id</span><span class="sxs-lookup"><span data-stu-id="254d1-116">-Id</span></span>
<span data-ttu-id="254d1-117">조직의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="254d1-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="254d1-118">-확인</span><span class="sxs-lookup"><span data-stu-id="254d1-118">-Confirm</span></span>
<span data-ttu-id="254d1-119">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="254d1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="254d1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="254d1-120">-WhatIf</span></span>
<span data-ttu-id="254d1-121">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="254d1-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="254d1-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="254d1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="254d1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="254d1-123">CommonParameters</span></span>
<span data-ttu-id="254d1-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="254d1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="254d1-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="254d1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="254d1-126">입력</span><span class="sxs-lookup"><span data-stu-id="254d1-126">INPUTS</span></span>

### <span data-ttu-id="254d1-127">System.String</span><span class="sxs-lookup"><span data-stu-id="254d1-127">System.String</span></span>

### <span data-ttu-id="254d1-128">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="254d1-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="254d1-129">출력</span><span class="sxs-lookup"><span data-stu-id="254d1-129">OUTPUTS</span></span>

### <span data-ttu-id="254d1-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="254d1-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="254d1-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="254d1-131">NOTES</span></span>

## <span data-ttu-id="254d1-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="254d1-132">RELATED LINKS</span></span>

[<span data-ttu-id="254d1-133">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="254d1-133">New-AzKeyVaultCertificateAdministratorDetail</span></span>](./New-AzKeyVaultCertificateAdministratorDetail.md)

