---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 2f4cab266cf63e1c33c35c051e9cc2b838f5b066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523040"
---
# <span data-ttu-id="86d87-101">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="86d87-101">Set-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="86d87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86d87-102">SYNOPSIS</span></span>
<span data-ttu-id="86d87-103">서비스 토폴로지에서 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="86d87-103">Updates a service in service topology.</span></span>

## <span data-ttu-id="86d87-104">구문과</span><span class="sxs-lookup"><span data-stu-id="86d87-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86d87-105">설명은</span><span class="sxs-lookup"><span data-stu-id="86d87-105">DESCRIPTION</span></span>
<span data-ttu-id="86d87-106">**AzureRmDeploymentManagerService** cmdlet은 지정 된 서비스 개체를 사용 하 여 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="86d87-106">The **Set-AzureRmDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="86d87-107">Cmdlet은 업데이트 된 서비스 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="86d87-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="86d87-108">예제의</span><span class="sxs-lookup"><span data-stu-id="86d87-108">EXAMPLES</span></span>

### <span data-ttu-id="86d87-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="86d87-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="86d87-110">이 명령은 이름, 서비스 토폴로지 이름 및 ResourceGroup이 $serviceObject의 Name, ServiceTopologyName 및 ResourceGroupName 속성과 각각 일치 하는 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="86d87-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="86d87-111">서비스가 $serviceObject에 설정 된 속성으로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="86d87-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="86d87-112">변수</span><span class="sxs-lookup"><span data-stu-id="86d87-112">PARAMETERS</span></span>

### <span data-ttu-id="86d87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86d87-113">-DefaultProfile</span></span>
<span data-ttu-id="86d87-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="86d87-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86d87-115">-서비스</span><span class="sxs-lookup"><span data-stu-id="86d87-115">-Service</span></span>
<span data-ttu-id="86d87-116">서비스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="86d87-116">The service object.</span></span>

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

### <span data-ttu-id="86d87-117">-확인</span><span class="sxs-lookup"><span data-stu-id="86d87-117">-Confirm</span></span>
<span data-ttu-id="86d87-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="86d87-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86d87-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86d87-119">-WhatIf</span></span>
<span data-ttu-id="86d87-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="86d87-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86d87-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86d87-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86d87-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d87-122">CommonParameters</span></span>
<span data-ttu-id="86d87-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="86d87-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86d87-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86d87-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d87-125">입력</span><span class="sxs-lookup"><span data-stu-id="86d87-125">INPUTS</span></span>

### <span data-ttu-id="86d87-126">Microsoft. Azure. PSServiceResource 명령)</span><span class="sxs-lookup"><span data-stu-id="86d87-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="86d87-127">출력</span><span class="sxs-lookup"><span data-stu-id="86d87-127">OUTPUTS</span></span>

### <span data-ttu-id="86d87-128">Microsoft. Azure. PSServiceResource 명령)</span><span class="sxs-lookup"><span data-stu-id="86d87-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="86d87-129">상속자</span><span class="sxs-lookup"><span data-stu-id="86d87-129">NOTES</span></span>

## <span data-ttu-id="86d87-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86d87-130">RELATED LINKS</span></span>

[<span data-ttu-id="86d87-131">새로운 AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="86d87-131">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="86d87-132">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="86d87-132">Get-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="86d87-133">제거-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="86d87-133">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)