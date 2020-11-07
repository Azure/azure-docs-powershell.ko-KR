---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 204ee5a7a4d0e5247ae3de239dce650deb4cff0c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875820"
---
# <span data-ttu-id="f0706-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f0706-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="f0706-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0706-102">SYNOPSIS</span></span>
<span data-ttu-id="f0706-103">키 자격 증명 모음에서 인증서 발급자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0706-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="f0706-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f0706-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0706-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f0706-105">DESCRIPTION</span></span>
<span data-ttu-id="f0706-106">**AzKeyVaultCertificateIssuer** cmdlet은 키 자격 증명 모음에서 인증서 발급자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0706-106">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="f0706-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f0706-107">EXAMPLES</span></span>

### <span data-ttu-id="f0706-108">예제 1: 인증서 발급자 제거</span><span class="sxs-lookup"><span data-stu-id="f0706-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="f0706-109">이 명령은 ContosoKV01 키 자격 증명 모음에서 TestIssuer01 이라는 인증서 발급자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0706-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="f0706-110">변수</span><span class="sxs-lookup"><span data-stu-id="f0706-110">PARAMETERS</span></span>

### <span data-ttu-id="f0706-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0706-111">-DefaultProfile</span></span>
<span data-ttu-id="f0706-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f0706-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0706-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f0706-113">-Force</span></span>
<span data-ttu-id="f0706-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0706-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0706-115">-이름</span><span class="sxs-lookup"><span data-stu-id="f0706-115">-Name</span></span>
<span data-ttu-id="f0706-116">제거할 발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0706-116">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0706-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0706-117">-PassThru</span></span>
<span data-ttu-id="f0706-118">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0706-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f0706-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0706-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0706-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f0706-120">-VaultName</span></span>
<span data-ttu-id="f0706-121">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0706-121">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0706-122">-확인</span><span class="sxs-lookup"><span data-stu-id="f0706-122">-Confirm</span></span>
<span data-ttu-id="f0706-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0706-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0706-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0706-124">-WhatIf</span></span>
<span data-ttu-id="f0706-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f0706-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0706-126">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f0706-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0706-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0706-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0706-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0706-128">CommonParameters</span></span>
<span data-ttu-id="f0706-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0706-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0706-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0706-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0706-131">입력</span><span class="sxs-lookup"><span data-stu-id="f0706-131">INPUTS</span></span>

### <span data-ttu-id="f0706-132">않아야</span><span class="sxs-lookup"><span data-stu-id="f0706-132">None</span></span>
<span data-ttu-id="f0706-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0706-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f0706-134">출력</span><span class="sxs-lookup"><span data-stu-id="f0706-134">OUTPUTS</span></span>

### <span data-ttu-id="f0706-135">Microsoft. KeyVault. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f0706-135">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="f0706-136">상속자</span><span class="sxs-lookup"><span data-stu-id="f0706-136">NOTES</span></span>

## <span data-ttu-id="f0706-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0706-137">RELATED LINKS</span></span>

[<span data-ttu-id="f0706-138">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f0706-138">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="f0706-139">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f0706-139">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


