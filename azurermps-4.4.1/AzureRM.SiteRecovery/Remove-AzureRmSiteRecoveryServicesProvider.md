---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 2FB62869-FF83-4D92-B08B-07AF3C393159
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: e7ee32974ef87b86d443d90b7dc628f9c9f1072f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529111"
---
# <span data-ttu-id="0f95b-101">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0f95b-101">Remove-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="0f95b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f95b-102">SYNOPSIS</span></span>
<span data-ttu-id="0f95b-103">Azure Site Recovery 서비스 공급자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f95b-103">Removes an Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f95b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0f95b-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f95b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0f95b-105">DESCRIPTION</span></span>
<span data-ttu-id="0f95b-106">**AzureRmSiteRecoveryServicesProvider** cmdlet은 자격 증명 모음에서 Azure Site Recovery 서비스 공급자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f95b-106">The **Remove-AzureRmSiteRecoveryServicesProvider** cmdlet removes an Azure Site Recovery Services Provider from the vault.</span></span>

## <span data-ttu-id="0f95b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0f95b-107">EXAMPLES</span></span>

## <span data-ttu-id="0f95b-108">변수</span><span class="sxs-lookup"><span data-stu-id="0f95b-108">PARAMETERS</span></span>

### <span data-ttu-id="0f95b-109">-Force</span><span class="sxs-lookup"><span data-stu-id="0f95b-109">-Force</span></span>
<span data-ttu-id="0f95b-110">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f95b-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0f95b-111">-서비스 공급자</span><span class="sxs-lookup"><span data-stu-id="0f95b-111">-ServicesProvider</span></span>
<span data-ttu-id="0f95b-112">서비스 공급자 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f95b-112">Specifies the Services Provider object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f95b-113">-확인</span><span class="sxs-lookup"><span data-stu-id="0f95b-113">-Confirm</span></span>
<span data-ttu-id="0f95b-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f95b-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f95b-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f95b-115">-WhatIf</span></span>
<span data-ttu-id="0f95b-116">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0f95b-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="0f95b-117">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f95b-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f95b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f95b-118">-DefaultProfile</span></span>
<span data-ttu-id="0f95b-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0f95b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f95b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f95b-120">CommonParameters</span></span>
<span data-ttu-id="0f95b-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f95b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f95b-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f95b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f95b-123">입력</span><span class="sxs-lookup"><span data-stu-id="0f95b-123">INPUTS</span></span>

### <span data-ttu-id="0f95b-124">Asrrecovery서비스 공급자</span><span class="sxs-lookup"><span data-stu-id="0f95b-124">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="0f95b-125">' 서비스 공급자 ' 매개 변수는 파이프라인에서 ' Asrrecovery서비스 공급자 '의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f95b-125">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="0f95b-126">출력</span><span class="sxs-lookup"><span data-stu-id="0f95b-126">OUTPUTS</span></span>

### <span data-ttu-id="0f95b-127">System.webserver. t e r ' 1 [[SiteRecovery Rjob, SiteRecovery, Version = 2.0.1.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="0f95b-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRJob, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0f95b-128">상속자</span><span class="sxs-lookup"><span data-stu-id="0f95b-128">NOTES</span></span>

## <span data-ttu-id="0f95b-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f95b-129">RELATED LINKS</span></span>

[<span data-ttu-id="0f95b-130">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0f95b-130">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="0f95b-131">업데이트-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0f95b-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
