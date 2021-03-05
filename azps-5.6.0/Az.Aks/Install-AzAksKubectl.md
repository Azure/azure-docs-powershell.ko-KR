---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 6a3dc975c34d4938235ce95743f73f833a948b49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966848"
---
# <span data-ttu-id="9333e-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="9333e-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="9333e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9333e-102">SYNOPSIS</span></span>
<span data-ttu-id="9333e-103">Kubernetes 명령줄 도구인 kubectl을 다운로드하고 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="9333e-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="9333e-104">구문</span><span class="sxs-lookup"><span data-stu-id="9333e-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9333e-105">설명</span><span class="sxs-lookup"><span data-stu-id="9333e-105">DESCRIPTION</span></span>
<span data-ttu-id="9333e-106">Kubernetes 명령줄 도구인 kubectl을 다운로드하고 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="9333e-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="9333e-107">예제</span><span class="sxs-lookup"><span data-stu-id="9333e-107">EXAMPLES</span></span>

### <span data-ttu-id="9333e-108">최신 버전의 kubectl 다운로드 및 설치</span><span class="sxs-lookup"><span data-stu-id="9333e-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="9333e-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9333e-109">PARAMETERS</span></span>

### <span data-ttu-id="9333e-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9333e-110">-AsJob</span></span>
<span data-ttu-id="9333e-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9333e-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9333e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9333e-112">-DefaultProfile</span></span>
<span data-ttu-id="9333e-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9333e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9333e-114">-대상</span><span class="sxs-lookup"><span data-stu-id="9333e-114">-Destination</span></span>
<span data-ttu-id="9333e-115">kubectl을 설치할 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="9333e-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="9333e-116">~/.azure-kubectl/에 설치하는 기본값</span><span class="sxs-lookup"><span data-stu-id="9333e-116">Default to install into ~/.azure-kubectl/</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9333e-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="9333e-117">-DownloadFromMirror</span></span>
<span data-ttu-id="9333e-118">미러 사이트에서 다운로드: https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="9333e-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

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

### <span data-ttu-id="9333e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9333e-119">-Force</span></span>
<span data-ttu-id="9333e-120">프롬프트 없이 기존 kubectl 덮어 덮어 덮어 사용</span><span class="sxs-lookup"><span data-stu-id="9333e-120">Overwrite existing kubectl without prompt</span></span>

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

### <span data-ttu-id="9333e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9333e-121">-PassThru</span></span>
<span data-ttu-id="9333e-122">{{ Fill PassThru 설명 }}</span><span class="sxs-lookup"><span data-stu-id="9333e-122">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="9333e-123">-Version</span><span class="sxs-lookup"><span data-stu-id="9333e-123">-Version</span></span>
<span data-ttu-id="9333e-124">설치할 kubectl 버전(예: 'v1.17.2').</span><span class="sxs-lookup"><span data-stu-id="9333e-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="9333e-125">기본값: 최신</span><span class="sxs-lookup"><span data-stu-id="9333e-125">Default value: Latest</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9333e-126">-확인</span><span class="sxs-lookup"><span data-stu-id="9333e-126">-Confirm</span></span>
<span data-ttu-id="9333e-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9333e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9333e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9333e-128">-WhatIf</span></span>
<span data-ttu-id="9333e-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9333e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9333e-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9333e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9333e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9333e-131">CommonParameters</span></span>
<span data-ttu-id="9333e-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9333e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9333e-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9333e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9333e-134">입력</span><span class="sxs-lookup"><span data-stu-id="9333e-134">INPUTS</span></span>

### <span data-ttu-id="9333e-135">없음</span><span class="sxs-lookup"><span data-stu-id="9333e-135">None</span></span>

## <span data-ttu-id="9333e-136">출력</span><span class="sxs-lookup"><span data-stu-id="9333e-136">OUTPUTS</span></span>

### <span data-ttu-id="9333e-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9333e-137">System.Boolean</span></span>

## <span data-ttu-id="9333e-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9333e-138">NOTES</span></span>

## <span data-ttu-id="9333e-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9333e-139">RELATED LINKS</span></span>
