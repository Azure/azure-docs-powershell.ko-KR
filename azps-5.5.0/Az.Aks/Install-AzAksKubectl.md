---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 746efc579e1977e54a1898bbe183d951c3d9c21f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199852"
---
# <span data-ttu-id="e3898-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="e3898-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="e3898-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3898-102">SYNOPSIS</span></span>
<span data-ttu-id="e3898-103">Kubernetes 명령줄 도구인 kubectl을 다운로드하여 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="e3898-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="e3898-104">구문</span><span class="sxs-lookup"><span data-stu-id="e3898-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3898-105">설명</span><span class="sxs-lookup"><span data-stu-id="e3898-105">DESCRIPTION</span></span>
<span data-ttu-id="e3898-106">Kubernetes 명령줄 도구인 kubectl을 다운로드하여 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="e3898-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="e3898-107">예제</span><span class="sxs-lookup"><span data-stu-id="e3898-107">EXAMPLES</span></span>

### <span data-ttu-id="e3898-108">최신 버전의 kubectl 다운로드 및 설치</span><span class="sxs-lookup"><span data-stu-id="e3898-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="e3898-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3898-109">PARAMETERS</span></span>

### <span data-ttu-id="e3898-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3898-110">-AsJob</span></span>
<span data-ttu-id="e3898-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e3898-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3898-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3898-112">-DefaultProfile</span></span>
<span data-ttu-id="e3898-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3898-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3898-114">-Destination</span><span class="sxs-lookup"><span data-stu-id="e3898-114">-Destination</span></span>
<span data-ttu-id="e3898-115">kubectl을 설치할 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="e3898-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="e3898-116">~/.azure-kubectl/에 기본적으로 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="e3898-116">Default to install into ~/.azure-kubectl/</span></span>

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

### <span data-ttu-id="e3898-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="e3898-117">-DownloadFromMirror</span></span>
<span data-ttu-id="e3898-118">미러 사이트에서 다운로드: https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="e3898-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

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

### <span data-ttu-id="e3898-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e3898-119">-Force</span></span>
<span data-ttu-id="e3898-120">프롬프트 없이 기존 kubectl 덮어 사용</span><span class="sxs-lookup"><span data-stu-id="e3898-120">Overwrite existing kubectl without prompt</span></span>

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

### <span data-ttu-id="e3898-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3898-121">-PassThru</span></span>
<span data-ttu-id="e3898-122">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="e3898-122">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="e3898-123">-Version</span><span class="sxs-lookup"><span data-stu-id="e3898-123">-Version</span></span>
<span data-ttu-id="e3898-124">설치할 kubectl 버전입니다(예: 'v1.17.2').</span><span class="sxs-lookup"><span data-stu-id="e3898-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="e3898-125">기본값: 최신</span><span class="sxs-lookup"><span data-stu-id="e3898-125">Default value: Latest</span></span>

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

### <span data-ttu-id="e3898-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3898-126">-Confirm</span></span>
<span data-ttu-id="e3898-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3898-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3898-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3898-128">-WhatIf</span></span>
<span data-ttu-id="e3898-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e3898-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3898-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3898-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3898-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3898-131">CommonParameters</span></span>
<span data-ttu-id="e3898-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e3898-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3898-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e3898-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3898-134">입력</span><span class="sxs-lookup"><span data-stu-id="e3898-134">INPUTS</span></span>

### <span data-ttu-id="e3898-135">없음</span><span class="sxs-lookup"><span data-stu-id="e3898-135">None</span></span>

## <span data-ttu-id="e3898-136">출력</span><span class="sxs-lookup"><span data-stu-id="e3898-136">OUTPUTS</span></span>

### <span data-ttu-id="e3898-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e3898-137">System.Boolean</span></span>

## <span data-ttu-id="e3898-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e3898-138">NOTES</span></span>

## <span data-ttu-id="e3898-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3898-139">RELATED LINKS</span></span>
