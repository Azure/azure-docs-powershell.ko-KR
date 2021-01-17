---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: ff280c11ff06d710eb8c74f88b839854506c6cd0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345794"
---
# <span data-ttu-id="daaab-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="daaab-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="daaab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daaab-102">SYNOPSIS</span></span>
<span data-ttu-id="daaab-103">Azure Site Recovery Services 공급자로부터 받은 정보를 새로 고침(서버 새로 고침)합니다.</span><span class="sxs-lookup"><span data-stu-id="daaab-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="daaab-104">구문</span><span class="sxs-lookup"><span data-stu-id="daaab-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="daaab-105">설명</span><span class="sxs-lookup"><span data-stu-id="daaab-105">DESCRIPTION</span></span>
<span data-ttu-id="daaab-106">**Update-AzRecoveryServicesAsrServicesProvider** cmdlet은 Azure Site Recovery Services 공급자로부터 받은 정보를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="daaab-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="daaab-107">이 cmdlet을 사용하여 Recovery Services 공급자로부터 받은 정보의 새로 고침을 트리거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="daaab-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="daaab-108">예제</span><span class="sxs-lookup"><span data-stu-id="daaab-108">EXAMPLES</span></span>

### <span data-ttu-id="daaab-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="daaab-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="daaab-110">지정된 ASR 서비스 공급자에서 정보를 새로 고침하는 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="daaab-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="daaab-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="daaab-111">PARAMETERS</span></span>

### <span data-ttu-id="daaab-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daaab-112">-DefaultProfile</span></span>
<span data-ttu-id="daaab-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="daaab-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="daaab-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="daaab-114">-InputObject</span></span>
<span data-ttu-id="daaab-115">정보를 업데이트(새로 고침)할 서버를 식별하는 ASR 서비스 공급자 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="daaab-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="daaab-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="daaab-116">-Confirm</span></span>
<span data-ttu-id="daaab-117">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="daaab-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daaab-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daaab-118">-WhatIf</span></span>
<span data-ttu-id="daaab-119">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="daaab-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="daaab-120">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="daaab-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daaab-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daaab-121">CommonParameters</span></span>
<span data-ttu-id="daaab-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="daaab-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daaab-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="daaab-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daaab-124">입력</span><span class="sxs-lookup"><span data-stu-id="daaab-124">INPUTS</span></span>

### <span data-ttu-id="daaab-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="daaab-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="daaab-126">출력</span><span class="sxs-lookup"><span data-stu-id="daaab-126">OUTPUTS</span></span>

### <span data-ttu-id="daaab-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="daaab-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="daaab-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="daaab-128">NOTES</span></span>

## <span data-ttu-id="daaab-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="daaab-129">RELATED LINKS</span></span>

[<span data-ttu-id="daaab-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="daaab-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="daaab-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="daaab-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
