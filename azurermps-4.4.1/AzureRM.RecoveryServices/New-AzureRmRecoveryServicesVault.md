---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: d9163e42b199dd5178e37a7d1bbe22abbb05c7f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527344"
---
# <span data-ttu-id="90067-101">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="90067-101">New-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="90067-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90067-102">SYNOPSIS</span></span>
<span data-ttu-id="90067-103">새 복구 서비스 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90067-103">Creates a new Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90067-104">구문과</span><span class="sxs-lookup"><span data-stu-id="90067-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90067-105">설명은</span><span class="sxs-lookup"><span data-stu-id="90067-105">DESCRIPTION</span></span>
<span data-ttu-id="90067-106">**AzureRmRecoveryServicesVault** cmdlet은 새 복구 서비스 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90067-106">The **New-AzureRmRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="90067-107">예제의</span><span class="sxs-lookup"><span data-stu-id="90067-107">EXAMPLES</span></span>

## <span data-ttu-id="90067-108">변수</span><span class="sxs-lookup"><span data-stu-id="90067-108">PARAMETERS</span></span>

### <span data-ttu-id="90067-109">-위치</span><span class="sxs-lookup"><span data-stu-id="90067-109">-Location</span></span>
<span data-ttu-id="90067-110">자격 증명 모음의 지리적 위치 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90067-110">Specifies the name of the geographic location of the vault.</span></span>

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

### <span data-ttu-id="90067-111">-이름</span><span class="sxs-lookup"><span data-stu-id="90067-111">-Name</span></span>
<span data-ttu-id="90067-112">만들 저장실의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90067-112">Specifies the name of the vault to create.</span></span>

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

### <span data-ttu-id="90067-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90067-113">-ResourceGroupName</span></span>
<span data-ttu-id="90067-114">지정 된 복구 서비스 개체를 만들거나 검색할 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90067-114">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="90067-115">-확인</span><span class="sxs-lookup"><span data-stu-id="90067-115">-Confirm</span></span>
<span data-ttu-id="90067-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="90067-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90067-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90067-117">-WhatIf</span></span>
<span data-ttu-id="90067-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="90067-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90067-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90067-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90067-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90067-120">-DefaultProfile</span></span>
<span data-ttu-id="90067-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90067-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90067-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90067-122">CommonParameters</span></span>
<span data-ttu-id="90067-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="90067-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90067-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90067-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90067-125">입력</span><span class="sxs-lookup"><span data-stu-id="90067-125">INPUTS</span></span>

## <span data-ttu-id="90067-126">출력</span><span class="sxs-lookup"><span data-stu-id="90067-126">OUTPUTS</span></span>

### <span data-ttu-id="90067-127">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="90067-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="90067-128">상속자</span><span class="sxs-lookup"><span data-stu-id="90067-128">NOTES</span></span>

## <span data-ttu-id="90067-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90067-129">RELATED LINKS</span></span>

[<span data-ttu-id="90067-130">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="90067-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="90067-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="90067-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="90067-132">제거-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="90067-132">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


