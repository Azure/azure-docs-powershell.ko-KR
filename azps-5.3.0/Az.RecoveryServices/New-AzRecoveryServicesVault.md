---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 3bb602d148b0843def129a1e4538d9ef8fdbe169
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492437"
---
# <span data-ttu-id="7692e-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7692e-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="7692e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7692e-102">SYNOPSIS</span></span>
<span data-ttu-id="7692e-103">새 Recovery Services 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7692e-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="7692e-104">구문</span><span class="sxs-lookup"><span data-stu-id="7692e-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7692e-105">설명</span><span class="sxs-lookup"><span data-stu-id="7692e-105">DESCRIPTION</span></span>
<span data-ttu-id="7692e-106">**New-AzRecoveryServicesVault** cmdlet은 새 Recovery Services 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7692e-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="7692e-107">예제</span><span class="sxs-lookup"><span data-stu-id="7692e-107">EXAMPLES</span></span>

### <span data-ttu-id="7692e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7692e-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="7692e-109">리소스 그룹 및 주어진 위치에 복구 서비스 자격 증명 모음을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7692e-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="7692e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7692e-110">PARAMETERS</span></span>

### <span data-ttu-id="7692e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7692e-111">-DefaultProfile</span></span>
<span data-ttu-id="7692e-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7692e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7692e-113">-Location</span><span class="sxs-lookup"><span data-stu-id="7692e-113">-Location</span></span>
<span data-ttu-id="7692e-114">자격 증명 모음의 지리적 위치 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7692e-114">Specifies the name of the geographic location of the vault.</span></span>

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

### <span data-ttu-id="7692e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7692e-115">-Name</span></span>
<span data-ttu-id="7692e-116">만들 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7692e-116">Specifies the name of the vault to create.</span></span>

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

### <span data-ttu-id="7692e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7692e-117">-ResourceGroupName</span></span>
<span data-ttu-id="7692e-118">지정된 Recovery Services 개체를 만들거나 검색할 Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7692e-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="7692e-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="7692e-119">-Tag</span></span>

<span data-ttu-id="7692e-120">Recovery Services 자격 증명 모음에 추가할 태그를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7692e-120">Specifies the Tags to add to the Recovery Services Vault</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7692e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7692e-121">-Confirm</span></span>
<span data-ttu-id="7692e-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7692e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7692e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7692e-123">-WhatIf</span></span>
<span data-ttu-id="7692e-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7692e-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7692e-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7692e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7692e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7692e-126">CommonParameters</span></span>
<span data-ttu-id="7692e-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7692e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7692e-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7692e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7692e-129">입력</span><span class="sxs-lookup"><span data-stu-id="7692e-129">INPUTS</span></span>

### <span data-ttu-id="7692e-130">없음</span><span class="sxs-lookup"><span data-stu-id="7692e-130">None</span></span>

## <span data-ttu-id="7692e-131">출력</span><span class="sxs-lookup"><span data-stu-id="7692e-131">OUTPUTS</span></span>

### <span data-ttu-id="7692e-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="7692e-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="7692e-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7692e-133">NOTES</span></span>

## <span data-ttu-id="7692e-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7692e-134">RELATED LINKS</span></span>

[<span data-ttu-id="7692e-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7692e-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="7692e-136">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7692e-136">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="7692e-137">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7692e-137">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


