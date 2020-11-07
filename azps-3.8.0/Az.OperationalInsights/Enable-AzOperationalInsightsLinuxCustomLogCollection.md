---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 99865242-6623-425E-92F2-0B229FC4EDAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 0cd64af058ecf9bbc1f42178d263fcf20cabc75f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877236"
---
# <span data-ttu-id="f3a4b-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="f3a4b-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="f3a4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="f3a4b-103">Linux 컴퓨터에서 사용자 지정 로그 수집을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a4b-103">Starts collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="f3a4b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3a4b-104">SYNTAX</span></span>

### <span data-ttu-id="f3a4b-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="f3a4b-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3a4b-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f3a4b-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3a4b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f3a4b-107">DESCRIPTION</span></span>
<span data-ttu-id="f3a4b-108">**AzOperationalInsightsLinuxCustomLogCollection** cmdlet은 연결 된 Linux 컴퓨터에서 작업 영역의 사용자 지정 로그 수집을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a4b-108">The **Enable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet starts collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="f3a4b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f3a4b-109">EXAMPLES</span></span>

## <span data-ttu-id="f3a4b-110">변수</span><span class="sxs-lookup"><span data-stu-id="f3a4b-110">PARAMETERS</span></span>

### <span data-ttu-id="f3a4b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3a4b-111">-DefaultProfile</span></span>
<span data-ttu-id="f3a4b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f3a4b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3a4b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3a4b-113">-ResourceGroupName</span></span>
<span data-ttu-id="f3a4b-114">Linux 컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a4b-114">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3a4b-115">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="f3a4b-115">-Workspace</span></span>
<span data-ttu-id="f3a4b-116">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a4b-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3a4b-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f3a4b-117">-WorkspaceName</span></span>
<span data-ttu-id="f3a4b-118">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a4b-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3a4b-119">-확인</span><span class="sxs-lookup"><span data-stu-id="f3a4b-119">-Confirm</span></span>
<span data-ttu-id="f3a4b-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a4b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3a4b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3a4b-121">-WhatIf</span></span>
<span data-ttu-id="f3a4b-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f3a4b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3a4b-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3a4b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3a4b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3a4b-124">CommonParameters</span></span>
<span data-ttu-id="f3a4b-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a4b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3a4b-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3a4b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3a4b-127">입력</span><span class="sxs-lookup"><span data-stu-id="f3a4b-127">INPUTS</span></span>

### <span data-ttu-id="f3a4b-128">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="f3a4b-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="f3a4b-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f3a4b-129">System.String</span></span>

## <span data-ttu-id="f3a4b-130">출력</span><span class="sxs-lookup"><span data-stu-id="f3a4b-130">OUTPUTS</span></span>

### <span data-ttu-id="f3a4b-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="f3a4b-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="f3a4b-132">상속자</span><span class="sxs-lookup"><span data-stu-id="f3a4b-132">NOTES</span></span>
* <span data-ttu-id="f3a4b-133">키워드: azure, azurerm, arm, resource, 관리, 관리자, 운영, insights</span><span class="sxs-lookup"><span data-stu-id="f3a4b-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="f3a4b-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3a4b-134">RELATED LINKS</span></span>

[<span data-ttu-id="f3a4b-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="f3a4b-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)


