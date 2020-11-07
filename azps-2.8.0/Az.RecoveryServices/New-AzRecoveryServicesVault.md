---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 65694116a924759c4cf29a7abcf95da7a03df39f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873522"
---
# <span data-ttu-id="f6bda-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f6bda-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="f6bda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6bda-102">SYNOPSIS</span></span>
<span data-ttu-id="f6bda-103">새 복구 서비스 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f6bda-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="f6bda-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f6bda-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6bda-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f6bda-105">DESCRIPTION</span></span>
<span data-ttu-id="f6bda-106">**AzRecoveryServicesVault** cmdlet은 새 복구 서비스 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f6bda-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="f6bda-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f6bda-107">EXAMPLES</span></span>

### <span data-ttu-id="f6bda-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f6bda-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="f6bda-109">리소스 그룹 및 지정 된 위치에 복구 서비스 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f6bda-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="f6bda-110">변수</span><span class="sxs-lookup"><span data-stu-id="f6bda-110">PARAMETERS</span></span>

### <span data-ttu-id="f6bda-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6bda-111">-DefaultProfile</span></span>
<span data-ttu-id="f6bda-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f6bda-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6bda-113">-위치</span><span class="sxs-lookup"><span data-stu-id="f6bda-113">-Location</span></span>
<span data-ttu-id="f6bda-114">자격 증명 모음의 지리적 위치 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6bda-114">Specifies the name of the geographic location of the vault.</span></span>

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

### <span data-ttu-id="f6bda-115">-이름</span><span class="sxs-lookup"><span data-stu-id="f6bda-115">-Name</span></span>
<span data-ttu-id="f6bda-116">만들 저장실의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6bda-116">Specifies the name of the vault to create.</span></span>

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

### <span data-ttu-id="f6bda-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6bda-117">-ResourceGroupName</span></span>
<span data-ttu-id="f6bda-118">지정 된 복구 서비스 개체를 만들거나 검색할 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6bda-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="f6bda-119">-확인</span><span class="sxs-lookup"><span data-stu-id="f6bda-119">-Confirm</span></span>
<span data-ttu-id="f6bda-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6bda-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6bda-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6bda-121">-WhatIf</span></span>
<span data-ttu-id="f6bda-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f6bda-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6bda-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f6bda-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6bda-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6bda-124">CommonParameters</span></span>
<span data-ttu-id="f6bda-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6bda-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6bda-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6bda-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6bda-127">입력</span><span class="sxs-lookup"><span data-stu-id="f6bda-127">INPUTS</span></span>

### <span data-ttu-id="f6bda-128">않아야</span><span class="sxs-lookup"><span data-stu-id="f6bda-128">None</span></span>

## <span data-ttu-id="f6bda-129">출력</span><span class="sxs-lookup"><span data-stu-id="f6bda-129">OUTPUTS</span></span>

### <span data-ttu-id="f6bda-130">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="f6bda-130">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="f6bda-131">상속자</span><span class="sxs-lookup"><span data-stu-id="f6bda-131">NOTES</span></span>

## <span data-ttu-id="f6bda-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6bda-132">RELATED LINKS</span></span>

[<span data-ttu-id="f6bda-133">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f6bda-133">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="f6bda-134">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f6bda-134">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="f6bda-135">제거-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f6bda-135">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


