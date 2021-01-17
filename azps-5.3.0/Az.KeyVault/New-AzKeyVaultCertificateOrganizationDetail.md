---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateorganizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
ms.openlocfilehash: 56b956aa8a65c4586859325f110f3ce593b2289c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491959"
---
# <span data-ttu-id="54e0e-101">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="54e0e-101">New-AzKeyVaultCertificateOrganizationDetail</span></span>

## <span data-ttu-id="54e0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54e0e-102">SYNOPSIS</span></span>
<span data-ttu-id="54e0e-103">메모리 내 인증서 조직 세부 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54e0e-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="54e0e-104">구문</span><span class="sxs-lookup"><span data-stu-id="54e0e-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetail [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54e0e-105">설명</span><span class="sxs-lookup"><span data-stu-id="54e0e-105">DESCRIPTION</span></span>
<span data-ttu-id="54e0e-106">**New-AzKeyVaultCertificateOrganizationDetail** cmdlet은 메모리 내 인증서 조직 세부 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54e0e-106">The **New-AzKeyVaultCertificateOrganizationDetail** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="54e0e-107">예제</span><span class="sxs-lookup"><span data-stu-id="54e0e-107">EXAMPLES</span></span>

### <span data-ttu-id="54e0e-108">예제 1: 조직 세부 정보 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="54e0e-108">Example 1: Create an organization details object</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails

Id AdministratorDetails
-- --------------------
   {Patti}
```

<span data-ttu-id="54e0e-109">첫 번째 명령은 인증서 관리자 세부 정보 개체를 만든 다음, $AdminDetails 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="54e0e-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>
<span data-ttu-id="54e0e-110">두 번째 명령은 인증서 조직 세부 정보를 만든 다음, 인증서 $OrgDetails 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="54e0e-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="54e0e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54e0e-111">PARAMETERS</span></span>

### <span data-ttu-id="54e0e-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="54e0e-112">-AdministratorDetails</span></span>
<span data-ttu-id="54e0e-113">인증서 조직 관리자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="54e0e-113">Specifies the certificate organization administrators.</span></span>

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

### <span data-ttu-id="54e0e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54e0e-114">-DefaultProfile</span></span>
<span data-ttu-id="54e0e-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="54e0e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54e0e-116">-Id</span><span class="sxs-lookup"><span data-stu-id="54e0e-116">-Id</span></span>
<span data-ttu-id="54e0e-117">조직의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="54e0e-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="54e0e-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54e0e-118">-Confirm</span></span>
<span data-ttu-id="54e0e-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="54e0e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54e0e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54e0e-120">-WhatIf</span></span>
<span data-ttu-id="54e0e-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="54e0e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54e0e-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54e0e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54e0e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54e0e-123">CommonParameters</span></span>
<span data-ttu-id="54e0e-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="54e0e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54e0e-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="54e0e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54e0e-126">입력</span><span class="sxs-lookup"><span data-stu-id="54e0e-126">INPUTS</span></span>

### <span data-ttu-id="54e0e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="54e0e-127">System.String</span></span>

### <span data-ttu-id="54e0e-128">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="54e0e-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="54e0e-129">출력</span><span class="sxs-lookup"><span data-stu-id="54e0e-129">OUTPUTS</span></span>

### <span data-ttu-id="54e0e-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="54e0e-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="54e0e-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="54e0e-131">NOTES</span></span>

## <span data-ttu-id="54e0e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54e0e-132">RELATED LINKS</span></span>

[<span data-ttu-id="54e0e-133">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="54e0e-133">New-AzKeyVaultCertificateAdministratorDetail</span></span>](./New-AzKeyVaultCertificateAdministratorDetail.md)

