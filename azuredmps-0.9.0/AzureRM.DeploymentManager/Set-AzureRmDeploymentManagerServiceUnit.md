---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: b04819f61f37b9bb47818a8b17e93db9a7cdb05d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523511"
---
# <span data-ttu-id="ea746-101">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="ea746-101">Set-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="ea746-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea746-102">SYNOPSIS</span></span>
<span data-ttu-id="ea746-103">서비스 단위를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea746-103">Updates a service unit.</span></span>

## <span data-ttu-id="ea746-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea746-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea746-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ea746-105">DESCRIPTION</span></span>
<span data-ttu-id="ea746-106">**AzureRmDeploymentManagerServiceUnit** cmdlet은 지정 된 서비스 단위 개체를 사용 하 여 서비스 단위를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea746-106">The **Set-AzureRmDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="ea746-107">Cmdlet은 업데이트 된 서비스 단위 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea746-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="ea746-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ea746-108">EXAMPLES</span></span>

### <span data-ttu-id="ea746-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="ea746-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="ea746-110">이 명령은 이름, 서비스 이름, 서비스 토폴로지 이름 및 ResourceGroup이 $serviceUnitObject의 Name, ServiceName, ServiceTopologyName 및 ResourceGroupName 속성과 각각 일치 하는 서비스 단위를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea746-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="ea746-111">명령이 업데이트 된 서비스 단위 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea746-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="ea746-112">변수</span><span class="sxs-lookup"><span data-stu-id="ea746-112">PARAMETERS</span></span>

### <span data-ttu-id="ea746-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea746-113">-DefaultProfile</span></span>
<span data-ttu-id="ea746-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea746-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea746-115">-ServiceUnit</span><span class="sxs-lookup"><span data-stu-id="ea746-115">-ServiceUnit</span></span>
<span data-ttu-id="ea746-116">서비스 단위 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ea746-116">The service unit object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea746-117">-확인</span><span class="sxs-lookup"><span data-stu-id="ea746-117">-Confirm</span></span>
<span data-ttu-id="ea746-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea746-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea746-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea746-119">-WhatIf</span></span>
<span data-ttu-id="ea746-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ea746-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea746-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea746-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea746-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea746-122">CommonParameters</span></span>
<span data-ttu-id="ea746-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea746-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea746-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea746-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea746-125">입력</span><span class="sxs-lookup"><span data-stu-id="ea746-125">INPUTS</span></span>

### <span data-ttu-id="ea746-126">Microsoft. Azure. Psservicemanager 리소스</span><span class="sxs-lookup"><span data-stu-id="ea746-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="ea746-127">출력</span><span class="sxs-lookup"><span data-stu-id="ea746-127">OUTPUTS</span></span>

### <span data-ttu-id="ea746-128">Microsoft. Azure. Psservicemanager 리소스</span><span class="sxs-lookup"><span data-stu-id="ea746-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="ea746-129">상속자</span><span class="sxs-lookup"><span data-stu-id="ea746-129">NOTES</span></span>

## <span data-ttu-id="ea746-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea746-130">RELATED LINKS</span></span>

[<span data-ttu-id="ea746-131">새로운 AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="ea746-131">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="ea746-132">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="ea746-132">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="ea746-133">제거-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="ea746-133">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)