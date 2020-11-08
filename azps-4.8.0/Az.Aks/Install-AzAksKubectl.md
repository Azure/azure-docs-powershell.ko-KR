---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 746efc579e1977e54a1898bbe183d951c3d9c21f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204159"
---
# <span data-ttu-id="21348-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="21348-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="21348-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21348-102">SYNOPSIS</span></span>
<span data-ttu-id="21348-103">Kubectl, Kubernetes 명령줄 도구를 다운로드 하 고 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="21348-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="21348-104">구문과</span><span class="sxs-lookup"><span data-stu-id="21348-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21348-105">설명은</span><span class="sxs-lookup"><span data-stu-id="21348-105">DESCRIPTION</span></span>
<span data-ttu-id="21348-106">Kubectl, Kubernetes 명령줄 도구를 다운로드 하 고 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="21348-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="21348-107">예제의</span><span class="sxs-lookup"><span data-stu-id="21348-107">EXAMPLES</span></span>

### <span data-ttu-id="21348-108">최신 버전의 kubectl 다운로드 및 설치</span><span class="sxs-lookup"><span data-stu-id="21348-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="21348-109">변수</span><span class="sxs-lookup"><span data-stu-id="21348-109">PARAMETERS</span></span>

### <span data-ttu-id="21348-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21348-110">-AsJob</span></span>
<span data-ttu-id="21348-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="21348-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21348-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21348-112">-DefaultProfile</span></span>
<span data-ttu-id="21348-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="21348-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21348-114">-대상</span><span class="sxs-lookup"><span data-stu-id="21348-114">-Destination</span></span>
<span data-ttu-id="21348-115">Kubectl를 설치할 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="21348-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="21348-116">~/.Azure-kubectl/에 설치 하는 기본</span><span class="sxs-lookup"><span data-stu-id="21348-116">Default to install into ~/.azure-kubectl/</span></span>

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

### <span data-ttu-id="21348-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="21348-117">-DownloadFromMirror</span></span>
<span data-ttu-id="21348-118">미러 사이트에서 다운로드: https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="21348-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

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

### <span data-ttu-id="21348-119">-Force</span><span class="sxs-lookup"><span data-stu-id="21348-119">-Force</span></span>
<span data-ttu-id="21348-120">묻지 않고 기존 kubectl 덮어쓰기</span><span class="sxs-lookup"><span data-stu-id="21348-120">Overwrite existing kubectl without prompt</span></span>

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

### <span data-ttu-id="21348-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21348-121">-PassThru</span></span>
<span data-ttu-id="21348-122">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="21348-122">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="21348-123">-버전</span><span class="sxs-lookup"><span data-stu-id="21348-123">-Version</span></span>
<span data-ttu-id="21348-124">설치할 kubectl 버전 (예: ' v 1.17.2 ')입니다.</span><span class="sxs-lookup"><span data-stu-id="21348-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="21348-125">기본값: 최신 값</span><span class="sxs-lookup"><span data-stu-id="21348-125">Default value: Latest</span></span>

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

### <span data-ttu-id="21348-126">-확인</span><span class="sxs-lookup"><span data-stu-id="21348-126">-Confirm</span></span>
<span data-ttu-id="21348-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="21348-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21348-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21348-128">-WhatIf</span></span>
<span data-ttu-id="21348-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="21348-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21348-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21348-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21348-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21348-131">CommonParameters</span></span>
<span data-ttu-id="21348-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="21348-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21348-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="21348-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21348-134">입력</span><span class="sxs-lookup"><span data-stu-id="21348-134">INPUTS</span></span>

### <span data-ttu-id="21348-135">않아야</span><span class="sxs-lookup"><span data-stu-id="21348-135">None</span></span>

## <span data-ttu-id="21348-136">출력</span><span class="sxs-lookup"><span data-stu-id="21348-136">OUTPUTS</span></span>

### <span data-ttu-id="21348-137">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="21348-137">System.Boolean</span></span>

## <span data-ttu-id="21348-138">상속자</span><span class="sxs-lookup"><span data-stu-id="21348-138">NOTES</span></span>

## <span data-ttu-id="21348-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21348-139">RELATED LINKS</span></span>
