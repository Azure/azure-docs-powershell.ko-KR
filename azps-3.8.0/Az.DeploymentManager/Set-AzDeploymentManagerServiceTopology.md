---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 4a9f785519710b7a6653b1ece27d7b526fceab31
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044362"
---
# <span data-ttu-id="a0cb4-101">Set-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="a0cb4-101">Set-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="a0cb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0cb4-102">SYNOPSIS</span></span>
<span data-ttu-id="a0cb4-103">서비스 토폴로지를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0cb4-103">Updates the service topology.</span></span>

## <span data-ttu-id="a0cb4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a0cb4-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0cb4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a0cb4-105">DESCRIPTION</span></span>
<span data-ttu-id="a0cb4-106">**AzDeploymentManagerServiceTopology** cmdlet은 지정 된 서비스 토폴로지 개체를 사용 하 여 서비스 토폴로지를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0cb4-106">The **Set-AzDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="a0cb4-107">Cmdlet은 업데이트 된 서비스 토폴로지 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0cb4-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="a0cb4-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a0cb4-108">EXAMPLES</span></span>

### <span data-ttu-id="a0cb4-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="a0cb4-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="a0cb4-110">이 명령은 name 및 ResourceGroup이 $serviceTopologyObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 서비스 토폴로지를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0cb4-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="a0cb4-111">명령이 업데이트 된 서비스 토폴로지 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0cb4-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="a0cb4-112">변수</span><span class="sxs-lookup"><span data-stu-id="a0cb4-112">PARAMETERS</span></span>

### <span data-ttu-id="a0cb4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0cb4-113">-DefaultProfile</span></span>
<span data-ttu-id="a0cb4-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a0cb4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0cb4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0cb4-115">-InputObject</span></span>
<span data-ttu-id="a0cb4-116">서비스 토폴로지 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a0cb4-116">The service topology object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0cb4-117">-확인</span><span class="sxs-lookup"><span data-stu-id="a0cb4-117">-Confirm</span></span>
<span data-ttu-id="a0cb4-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0cb4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0cb4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0cb4-119">-WhatIf</span></span>
<span data-ttu-id="a0cb4-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a0cb4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0cb4-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0cb4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0cb4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0cb4-122">CommonParameters</span></span>
<span data-ttu-id="a0cb4-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0cb4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0cb4-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a0cb4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0cb4-125">입력</span><span class="sxs-lookup"><span data-stu-id="a0cb4-125">INPUTS</span></span>

### <span data-ttu-id="a0cb4-126">PSServiceTopologyResource-. m i 매니저.</span><span class="sxs-lookup"><span data-stu-id="a0cb4-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="a0cb4-127">출력</span><span class="sxs-lookup"><span data-stu-id="a0cb4-127">OUTPUTS</span></span>

### <span data-ttu-id="a0cb4-128">PSServiceTopologyResource-. m i 매니저.</span><span class="sxs-lookup"><span data-stu-id="a0cb4-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="a0cb4-129">상속자</span><span class="sxs-lookup"><span data-stu-id="a0cb4-129">NOTES</span></span>

## <span data-ttu-id="a0cb4-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0cb4-130">RELATED LINKS</span></span>
