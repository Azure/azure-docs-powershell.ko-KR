---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 061b16758386cf2e279250a1ab72cdcf4180a1f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211728"
---
# <span data-ttu-id="238a6-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="238a6-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="238a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="238a6-102">SYNOPSIS</span></span>
<span data-ttu-id="238a6-103">키 자격 증명 모음에서 인증서 발급자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="238a6-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="238a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="238a6-104">SYNTAX</span></span>

### <span data-ttu-id="238a6-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="238a6-105">Default (Default)</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="238a6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="238a6-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="238a6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="238a6-107">DESCRIPTION</span></span>
<span data-ttu-id="238a6-108">**AzKeyVaultCertificateIssuer** cmdlet은 키 자격 증명 모음에서 인증서 발급자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="238a6-108">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="238a6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="238a6-109">EXAMPLES</span></span>

### <span data-ttu-id="238a6-110">예제 1: 인증서 발급자 제거</span><span class="sxs-lookup"><span data-stu-id="238a6-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="238a6-111">이 명령은 ContosoKV01 키 자격 증명 모음에서 TestIssuer01 이라는 인증서 발급자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="238a6-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="238a6-112">변수</span><span class="sxs-lookup"><span data-stu-id="238a6-112">PARAMETERS</span></span>

### <span data-ttu-id="238a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="238a6-113">-DefaultProfile</span></span>
<span data-ttu-id="238a6-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="238a6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="238a6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="238a6-115">-Force</span></span>
<span data-ttu-id="238a6-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="238a6-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="238a6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="238a6-117">-InputObject</span></span>
<span data-ttu-id="238a6-118">인증서 발급자 개체</span><span class="sxs-lookup"><span data-stu-id="238a6-118">Certificate Issuer Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="238a6-119">-이름</span><span class="sxs-lookup"><span data-stu-id="238a6-119">-Name</span></span>
<span data-ttu-id="238a6-120">제거할 발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="238a6-120">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="238a6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="238a6-121">-PassThru</span></span>
<span data-ttu-id="238a6-122">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="238a6-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="238a6-123">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="238a6-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="238a6-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="238a6-124">-VaultName</span></span>
<span data-ttu-id="238a6-125">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="238a6-125">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="238a6-126">-확인</span><span class="sxs-lookup"><span data-stu-id="238a6-126">-Confirm</span></span>
<span data-ttu-id="238a6-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="238a6-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="238a6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="238a6-128">-WhatIf</span></span>
<span data-ttu-id="238a6-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="238a6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="238a6-130">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="238a6-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="238a6-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="238a6-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="238a6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="238a6-132">CommonParameters</span></span>
<span data-ttu-id="238a6-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="238a6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="238a6-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="238a6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="238a6-135">입력</span><span class="sxs-lookup"><span data-stu-id="238a6-135">INPUTS</span></span>

### <span data-ttu-id="238a6-136">Microsoft. KeyVault. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="238a6-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="238a6-137">출력</span><span class="sxs-lookup"><span data-stu-id="238a6-137">OUTPUTS</span></span>

### <span data-ttu-id="238a6-138">Microsoft. KeyVault. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="238a6-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="238a6-139">상속자</span><span class="sxs-lookup"><span data-stu-id="238a6-139">NOTES</span></span>

## <span data-ttu-id="238a6-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="238a6-140">RELATED LINKS</span></span>

[<span data-ttu-id="238a6-141">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="238a6-141">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="238a6-142">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="238a6-142">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


