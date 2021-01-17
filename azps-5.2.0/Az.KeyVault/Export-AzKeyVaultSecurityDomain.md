---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/export-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: 94f27b497450201715b423babbd55811f2382dd2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372786"
---
# <span data-ttu-id="b512a-101">Export-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="b512a-101">Export-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="b512a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b512a-102">SYNOPSIS</span></span>
<span data-ttu-id="b512a-103">관리되는 HSM의 보안 도메인 데이터를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b512a-103">Exports the security domain data of a managed HSM.</span></span>

## <span data-ttu-id="b512a-104">구문</span><span class="sxs-lookup"><span data-stu-id="b512a-104">SYNTAX</span></span>

### <span data-ttu-id="b512a-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="b512a-105">ByName (Default)</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b512a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b512a-106">ByInputObject</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b512a-107">설명</span><span class="sxs-lookup"><span data-stu-id="b512a-107">DESCRIPTION</span></span>
<span data-ttu-id="b512a-108">다른 HSM에서 가져오기 위해 관리되는 HSM의 보안 도메인 데이터를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b512a-108">Exports the security domain data of a managed HSM for importing on another HSM.</span></span>

## <span data-ttu-id="b512a-109">예제</span><span class="sxs-lookup"><span data-stu-id="b512a-109">EXAMPLES</span></span>

### <span data-ttu-id="b512a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b512a-110">Example 1</span></span>
```powershell
PS C:\Users\username\> Export-AzKeyVaultSecurityDomain -Name testmhsm -Certificates {pathOfCertificates}/sd1.cer, {pathOfCertificates}/sd2.cer, {pathOfCertificates}/sd3.cer -OutputPath {pathOfOutput}/sd.ps.json -Quorum 2
```

<span data-ttu-id="b512a-111">이 명령은 testmhsm이라는 관리되는 HSM을 검색하고 해당 관리되는 HSM 보안 도메인의 백업을 지정된 출력 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b512a-111">This command retrieves the managed HSM named testmhsm and saves a backup of that managed HSM security domain to the specified output file.</span></span>

## <span data-ttu-id="b512a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b512a-112">PARAMETERS</span></span>

### <span data-ttu-id="b512a-113">-Certificates</span><span class="sxs-lookup"><span data-stu-id="b512a-113">-Certificates</span></span>
<span data-ttu-id="b512a-114">보안 도메인 데이터를 암호화하는 데 사용되는 인증서에 대한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="b512a-114">Paths to the certificates that are used to encrypt the security domain data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b512a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b512a-115">-DefaultProfile</span></span>
<span data-ttu-id="b512a-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b512a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b512a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b512a-117">-Force</span></span>
<span data-ttu-id="b512a-118">기존 파일을 덮어 사용할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b512a-118">Specify whether to overwrite existing file.</span></span>

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

### <span data-ttu-id="b512a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b512a-119">-InputObject</span></span>
<span data-ttu-id="b512a-120">관리되는 HSM을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b512a-120">Object representing a managed HSM.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b512a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b512a-121">-Name</span></span>
<span data-ttu-id="b512a-122">관리되는 HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b512a-122">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b512a-123">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="b512a-123">-OutputPath</span></span>
<span data-ttu-id="b512a-124">보안 도메인 데이터를 다운로드할 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b512a-124">Specify the path where security domain data will be downloaded to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b512a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b512a-125">-PassThru</span></span>
<span data-ttu-id="b512a-126">지정하면 cmdlet이 성공하면 부울이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="b512a-126">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="b512a-127">-Quorum</span><span class="sxs-lookup"><span data-stu-id="b512a-127">-Quorum</span></span>
<span data-ttu-id="b512a-128">복구를 위해 보안 도메인의 암호를 해독하는 데 필요한 최소 공유 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b512a-128">The minimum number of shares required to decrypt the security domain for recovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b512a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b512a-129">-Confirm</span></span>
<span data-ttu-id="b512a-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b512a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b512a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b512a-131">-WhatIf</span></span>
<span data-ttu-id="b512a-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b512a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b512a-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b512a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b512a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b512a-134">CommonParameters</span></span>
<span data-ttu-id="b512a-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b512a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b512a-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b512a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b512a-137">입력</span><span class="sxs-lookup"><span data-stu-id="b512a-137">INPUTS</span></span>

### <span data-ttu-id="b512a-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b512a-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="b512a-139">출력</span><span class="sxs-lookup"><span data-stu-id="b512a-139">OUTPUTS</span></span>

### <span data-ttu-id="b512a-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b512a-140">System.Boolean</span></span>

## <span data-ttu-id="b512a-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b512a-141">NOTES</span></span>

## <span data-ttu-id="b512a-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b512a-142">RELATED LINKS</span></span>
