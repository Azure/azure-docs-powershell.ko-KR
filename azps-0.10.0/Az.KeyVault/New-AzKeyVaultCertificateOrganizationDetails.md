---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificateorganizationdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetails.md
ms.openlocfilehash: 76208f8d4c1b8b1b463ea5a0f24a4e34e7a82855
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876705"
---
# <span data-ttu-id="8a195-101">New-AzKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="8a195-101">New-AzKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="8a195-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a195-102">SYNOPSIS</span></span>
<span data-ttu-id="8a195-103">메모리 내 인증서 조직 세부 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8a195-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="8a195-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a195-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a195-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8a195-105">DESCRIPTION</span></span>
<span data-ttu-id="8a195-106">**AzKeyVaultCertificateOrganizationDetails** cmdlet은 메모리 내 인증서 조직 세부 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8a195-106">The **New-AzKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="8a195-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8a195-107">EXAMPLES</span></span>

### <span data-ttu-id="8a195-108">예제 1: 조직 세부 정보 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="8a195-108">Example 1: Create an organization details object</span></span>
```
PS C:\>$AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
$OrgDetails = New-AzKeyVaultCertificateOrganizationDetails -Name "Contoso" -Address1 "1 Redmond Way" -Address2 "Suite 906" -City "Redmond" -State "WA" -Zip 98052 -Country "US" -AdministratorDetails $AdminDetails
```

<span data-ttu-id="8a195-109">첫 번째 명령은 인증서 관리자 세부 정보 개체를 만든 다음 $AdminDetails 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a195-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

<span data-ttu-id="8a195-110">두 번째 명령은 인증서 조직 세부 정보 개체를 만든 다음 $OrgDetails 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a195-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="8a195-111">변수</span><span class="sxs-lookup"><span data-stu-id="8a195-111">PARAMETERS</span></span>

### <span data-ttu-id="8a195-112">-관리자 세부 정보</span><span class="sxs-lookup"><span data-stu-id="8a195-112">-AdministratorDetails</span></span>
<span data-ttu-id="8a195-113">인증서 조직 관리자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a195-113">Specifies the certificate organization administrators.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a195-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a195-114">-DefaultProfile</span></span>
<span data-ttu-id="8a195-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8a195-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a195-116">-Id</span><span class="sxs-lookup"><span data-stu-id="8a195-116">-Id</span></span>
<span data-ttu-id="8a195-117">조직의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a195-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="8a195-118">-확인</span><span class="sxs-lookup"><span data-stu-id="8a195-118">-Confirm</span></span>
<span data-ttu-id="8a195-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a195-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a195-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a195-120">-WhatIf</span></span>
<span data-ttu-id="8a195-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8a195-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a195-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8a195-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a195-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a195-123">CommonParameters</span></span>
<span data-ttu-id="8a195-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a195-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a195-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a195-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a195-126">입력</span><span class="sxs-lookup"><span data-stu-id="8a195-126">INPUTS</span></span>

### <span data-ttu-id="8a195-127">않아야</span><span class="sxs-lookup"><span data-stu-id="8a195-127">None</span></span>
<span data-ttu-id="8a195-128">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8a195-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8a195-129">출력</span><span class="sxs-lookup"><span data-stu-id="8a195-129">OUTPUTS</span></span>

### <span data-ttu-id="8a195-130">Microsoft. KeyVault. KeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="8a195-130">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="8a195-131">상속자</span><span class="sxs-lookup"><span data-stu-id="8a195-131">NOTES</span></span>

## <span data-ttu-id="8a195-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a195-132">RELATED LINKS</span></span>

[<span data-ttu-id="8a195-133">새로운 AzKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="8a195-133">New-AzKeyVaultCertificateAdministratorDetails</span></span>](./New-AzKeyVaultCertificateAdministratorDetails.md)

