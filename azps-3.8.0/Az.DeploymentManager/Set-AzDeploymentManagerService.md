---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: fb3f7ccab164370e1c55992a666ac7256b5a4a95
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044364"
---
# <span data-ttu-id="ad007-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="ad007-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="ad007-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad007-102">SYNOPSIS</span></span>
<span data-ttu-id="ad007-103">서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad007-103">Updates the service.</span></span>

## <span data-ttu-id="ad007-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad007-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad007-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ad007-105">DESCRIPTION</span></span>
<span data-ttu-id="ad007-106">**AzDeploymentManagerService** cmdlet은 지정 된 서비스 개체를 사용 하 여 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad007-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="ad007-107">Cmdlet은 업데이트 된 서비스 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad007-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="ad007-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ad007-108">EXAMPLES</span></span>

### <span data-ttu-id="ad007-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="ad007-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="ad007-110">이 명령은 이름, 서비스 토폴로지 이름 및 ResourceGroup이 $serviceObject의 Name, ServiceTopologyName 및 ResourceGroupName 속성과 각각 일치 하는 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad007-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="ad007-111">서비스가 $serviceObject에 설정 된 속성으로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad007-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="ad007-112">변수</span><span class="sxs-lookup"><span data-stu-id="ad007-112">PARAMETERS</span></span>

### <span data-ttu-id="ad007-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad007-113">-DefaultProfile</span></span>
<span data-ttu-id="ad007-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad007-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad007-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad007-115">-InputObject</span></span>
<span data-ttu-id="ad007-116">서비스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ad007-116">The service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad007-117">-확인</span><span class="sxs-lookup"><span data-stu-id="ad007-117">-Confirm</span></span>
<span data-ttu-id="ad007-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad007-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad007-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad007-119">-WhatIf</span></span>
<span data-ttu-id="ad007-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad007-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad007-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad007-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad007-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad007-122">CommonParameters</span></span>
<span data-ttu-id="ad007-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad007-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad007-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ad007-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad007-125">입력</span><span class="sxs-lookup"><span data-stu-id="ad007-125">INPUTS</span></span>

### <span data-ttu-id="ad007-126">Microsoft. Azure. PSServiceResource 명령)</span><span class="sxs-lookup"><span data-stu-id="ad007-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="ad007-127">출력</span><span class="sxs-lookup"><span data-stu-id="ad007-127">OUTPUTS</span></span>

### <span data-ttu-id="ad007-128">Microsoft. Azure. PSServiceResource 명령)</span><span class="sxs-lookup"><span data-stu-id="ad007-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="ad007-129">상속자</span><span class="sxs-lookup"><span data-stu-id="ad007-129">NOTES</span></span>

## <span data-ttu-id="ad007-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad007-130">RELATED LINKS</span></span>
