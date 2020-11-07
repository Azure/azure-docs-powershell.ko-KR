---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3302054E-C5BB-4B89-B9C9-ED7572DFA234
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 7c7afc0a1b6544f165f379a7363960142f73780d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703960"
---
# <span data-ttu-id="dc446-101">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="dc446-101">Remove-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="dc446-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc446-102">SYNOPSIS</span></span>
<span data-ttu-id="dc446-103">현재 자격 증명 모음에서 사이트 복구 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc446-103">Removes a Site Recovery server from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc446-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dc446-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServer -Server <ASRServer> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc446-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dc446-105">DESCRIPTION</span></span>
<span data-ttu-id="dc446-106">AzureRmSiteRecoveryServer cmdlet은 현재 자격 증명 모음에서 제거 하는 Azure Site Recovery 서버의 등록을 **취소** 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc446-106">The **Remove-AzureRmSiteRecoveryServer** cmdlet unregisters an Azure Site Recovery server which removes it from the current vault.</span></span>

## <span data-ttu-id="dc446-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dc446-107">EXAMPLES</span></span>

## <span data-ttu-id="dc446-108">변수</span><span class="sxs-lookup"><span data-stu-id="dc446-108">PARAMETERS</span></span>

### <span data-ttu-id="dc446-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc446-109">-DefaultProfile</span></span>
<span data-ttu-id="dc446-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc446-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc446-111">-Force</span><span class="sxs-lookup"><span data-stu-id="dc446-111">-Force</span></span>
<span data-ttu-id="dc446-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc446-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dc446-113">-서버</span><span class="sxs-lookup"><span data-stu-id="dc446-113">-Server</span></span>
<span data-ttu-id="dc446-114">사이트 복구 서버 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc446-114">Specifies the Site Recovery server object.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc446-115">-확인</span><span class="sxs-lookup"><span data-stu-id="dc446-115">-Confirm</span></span>
<span data-ttu-id="dc446-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc446-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc446-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc446-117">-WhatIf</span></span>
<span data-ttu-id="dc446-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dc446-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="dc446-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc446-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc446-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc446-120">CommonParameters</span></span>
<span data-ttu-id="dc446-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc446-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc446-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc446-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc446-123">입력</span><span class="sxs-lookup"><span data-stu-id="dc446-123">INPUTS</span></span>

### <span data-ttu-id="dc446-124">ASRServer</span><span class="sxs-lookup"><span data-stu-id="dc446-124">ASRServer</span></span>
<span data-ttu-id="dc446-125">' Server ' 매개 변수는 파이프라인에서 ' ASRServer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc446-125">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="dc446-126">출력</span><span class="sxs-lookup"><span data-stu-id="dc446-126">OUTPUTS</span></span>

### <span data-ttu-id="dc446-127">System.webserver. t e r ' 1 [SiteRecovery], 또는.</span><span class="sxs-lookup"><span data-stu-id="dc446-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="dc446-128">상속자</span><span class="sxs-lookup"><span data-stu-id="dc446-128">NOTES</span></span>

## <span data-ttu-id="dc446-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc446-129">RELATED LINKS</span></span>

[<span data-ttu-id="dc446-130">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="dc446-130">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="dc446-131">업데이트-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="dc446-131">Update-AzureRmSiteRecoveryServer</span></span>](./Update-AzureRmSiteRecoveryServer.md)
