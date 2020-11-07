---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: EF3FE3F1-1C8F-41EB-990E-F2B30BD9D082
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 94706768c6e5f222abe5a74ea32549f356abe1c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877247"
---
# <span data-ttu-id="fd5b0-101">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="fd5b0-101">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="fd5b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd5b0-102">SYNOPSIS</span></span>
<span data-ttu-id="fd5b0-103">Linux 컴퓨터에서 사용자 지정 로그 수집을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd5b0-103">Stops collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="fd5b0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fd5b0-104">SYNTAX</span></span>

### <span data-ttu-id="fd5b0-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="fd5b0-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd5b0-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fd5b0-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd5b0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fd5b0-107">DESCRIPTION</span></span>
<span data-ttu-id="fd5b0-108">**AzOperationalInsightsLinuxCustomLogCollection** cmdlet은 작업 영역에서 연결 된 Linux 컴퓨터의 사용자 지정 로그 수집을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd5b0-108">The **Disable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet stops collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="fd5b0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fd5b0-109">EXAMPLES</span></span>

## <span data-ttu-id="fd5b0-110">변수</span><span class="sxs-lookup"><span data-stu-id="fd5b0-110">PARAMETERS</span></span>

### <span data-ttu-id="fd5b0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd5b0-111">-DefaultProfile</span></span>
<span data-ttu-id="fd5b0-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fd5b0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd5b0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd5b0-113">-ResourceGroupName</span></span>
<span data-ttu-id="fd5b0-114">Linux 컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd5b0-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="fd5b0-115">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="fd5b0-115">-Workspace</span></span>
<span data-ttu-id="fd5b0-116">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd5b0-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="fd5b0-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fd5b0-117">-WorkspaceName</span></span>
<span data-ttu-id="fd5b0-118">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd5b0-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="fd5b0-119">-확인</span><span class="sxs-lookup"><span data-stu-id="fd5b0-119">-Confirm</span></span>
<span data-ttu-id="fd5b0-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd5b0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd5b0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd5b0-121">-WhatIf</span></span>
<span data-ttu-id="fd5b0-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fd5b0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd5b0-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd5b0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd5b0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd5b0-124">CommonParameters</span></span>
<span data-ttu-id="fd5b0-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd5b0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd5b0-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd5b0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd5b0-127">입력</span><span class="sxs-lookup"><span data-stu-id="fd5b0-127">INPUTS</span></span>

### <span data-ttu-id="fd5b0-128">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="fd5b0-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="fd5b0-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fd5b0-129">System.String</span></span>

## <span data-ttu-id="fd5b0-130">출력</span><span class="sxs-lookup"><span data-stu-id="fd5b0-130">OUTPUTS</span></span>

### <span data-ttu-id="fd5b0-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="fd5b0-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="fd5b0-132">상속자</span><span class="sxs-lookup"><span data-stu-id="fd5b0-132">NOTES</span></span>
* <span data-ttu-id="fd5b0-133">키워드: azure, azurerm, arm, resource, 관리, 관리자, 운영, insights</span><span class="sxs-lookup"><span data-stu-id="fd5b0-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="fd5b0-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd5b0-134">RELATED LINKS</span></span>

[<span data-ttu-id="fd5b0-135">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="fd5b0-135">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


