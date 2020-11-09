---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmSecurityDomain.md
ms.openlocfilehash: 10a54afa8a6ef2e37beebd9d6cdcd304b2d13979
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304622"
---
# <span data-ttu-id="1f691-101">Backup-AzManagedHsmSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="1f691-101">Backup-AzManagedHsmSecurityDomain</span></span>

## <span data-ttu-id="1f691-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f691-102">SYNOPSIS</span></span>
<span data-ttu-id="1f691-103">복원을 위해 관리 되는 HSM의 보안 도메인 데이터를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f691-103">Backs up the security domain data of a managed HSM for restoring.</span></span>

## <span data-ttu-id="1f691-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f691-104">SYNTAX</span></span>

### <span data-ttu-id="1f691-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="1f691-105">ByName (Default)</span></span>
```
Backup-AzManagedHsmSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f691-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1f691-106">ByInputObject</span></span>
```
Backup-AzManagedHsmSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f691-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1f691-107">DESCRIPTION</span></span>
<span data-ttu-id="1f691-108">이 cmdlet은 복원을 위해 관리 되는 HSM의 보안 도메인 데이터를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f691-108">This cmdlet backs up the security domain data of a managed HSM for restoring.</span></span>

## <span data-ttu-id="1f691-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1f691-109">EXAMPLES</span></span>

### <span data-ttu-id="1f691-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1f691-110">Example 1</span></span>
```powershell
PS C:\Users\username\> Backup-AzManagedHsmSecurityDomain -Name testmhsm -Certificates {pathOfCertificates}/sd1.cer, {pathOfCertificates}/sd2.cer, {pathOfCertificates}/sd3.cer -OutputPath {pathOfOutput}/sd.ps.json -Quorum 2
```

<span data-ttu-id="1f691-111">이 명령은 testmhsm 이라는 관리 되는 HSM을 검색 하 고 관리 되는 HSM 보안 도메인의 백업을 지정 된 출력 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f691-111">This command retrieves the managed HSM named testmhsm and saves a backup of that managed HSM security domain to the specified output file.</span></span>

## <span data-ttu-id="1f691-112">변수</span><span class="sxs-lookup"><span data-stu-id="1f691-112">PARAMETERS</span></span>

### <span data-ttu-id="1f691-113">-인증서</span><span class="sxs-lookup"><span data-stu-id="1f691-113">-Certificates</span></span>
<span data-ttu-id="1f691-114">보안 도메인 데이터를 암호화 하는 데 사용 되는 인증서의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="1f691-114">Paths to the certificates that are used to encrypt the security domain data.</span></span>

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

### <span data-ttu-id="1f691-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f691-115">-DefaultProfile</span></span>
<span data-ttu-id="1f691-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f691-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f691-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1f691-117">-Force</span></span>
<span data-ttu-id="1f691-118">기존 파일을 덮어쓸지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f691-118">Specify whether to overwrite existing file.</span></span>

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

### <span data-ttu-id="1f691-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f691-119">-InputObject</span></span>
<span data-ttu-id="1f691-120">관리 되는 HSM을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1f691-120">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="1f691-121">-이름</span><span class="sxs-lookup"><span data-stu-id="1f691-121">-Name</span></span>
<span data-ttu-id="1f691-122">관리 되는 HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f691-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="1f691-123">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="1f691-123">-OutputPath</span></span>
<span data-ttu-id="1f691-124">보안 도메인 데이터를 다운로드 하는 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f691-124">Specify the path where security domain data will be downloaded to.</span></span>

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

### <span data-ttu-id="1f691-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f691-125">-PassThru</span></span>
<span data-ttu-id="1f691-126">지정 되 면 cmdlet이 성공할 때 부울이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f691-126">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="1f691-127">-쿼럼</span><span class="sxs-lookup"><span data-stu-id="1f691-127">-Quorum</span></span>
<span data-ttu-id="1f691-128">복구를 위해 보안 도메인을 해독 하는 데 필요한 최소 공유 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1f691-128">The minimum number of shares required to decrypt the security domain for recovery.</span></span>

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

### <span data-ttu-id="1f691-129">-확인</span><span class="sxs-lookup"><span data-stu-id="1f691-129">-Confirm</span></span>
<span data-ttu-id="1f691-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f691-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f691-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f691-131">-WhatIf</span></span>
<span data-ttu-id="1f691-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f691-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f691-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f691-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f691-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f691-134">CommonParameters</span></span>
<span data-ttu-id="1f691-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f691-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f691-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f691-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f691-137">입력</span><span class="sxs-lookup"><span data-stu-id="1f691-137">INPUTS</span></span>

### <span data-ttu-id="1f691-138">Microsoft. KeyVault. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1f691-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="1f691-139">출력</span><span class="sxs-lookup"><span data-stu-id="1f691-139">OUTPUTS</span></span>

### <span data-ttu-id="1f691-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1f691-140">System.Boolean</span></span>

## <span data-ttu-id="1f691-141">상속자</span><span class="sxs-lookup"><span data-stu-id="1f691-141">NOTES</span></span>

## <span data-ttu-id="1f691-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f691-142">RELATED LINKS</span></span>
