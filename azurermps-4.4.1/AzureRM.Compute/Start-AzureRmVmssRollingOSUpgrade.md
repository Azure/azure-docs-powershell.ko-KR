---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmssRollingOSUpgrade.md
ms.openlocfilehash: 7f4e28c00b0238b519ad2b038676a295147b5c0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532316"
---
# <span data-ttu-id="de35b-101">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="de35b-101">Start-AzureRmVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="de35b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de35b-102">SYNOPSIS</span></span>
<span data-ttu-id="de35b-103">모든 가상 컴퓨터 크기 집합 인스턴스를 사용 가능한 최신 플랫폼 이미지 OS 버전으로 이동 하기 위해 롤링 업그레이드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="de35b-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de35b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="de35b-104">SYNTAX</span></span>

```
Start-AzureRmVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de35b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="de35b-105">DESCRIPTION</span></span>
<span data-ttu-id="de35b-106">모든 가상 컴퓨터 크기 집합 인스턴스를 사용 가능한 최신 플랫폼 이미지 OS 버전으로 이동 하기 위해 롤링 업그레이드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="de35b-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="de35b-107">사용 가능한 최신 OS 버전을 이미 실행 중인 인스턴스는 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="de35b-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="de35b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="de35b-108">EXAMPLES</span></span>

### <span data-ttu-id="de35b-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="de35b-109">Example 1</span></span>
```
PS C:\> Start-AzureRmVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="de35b-110">이 명령은 리소스 그룹 "Group001"의 VM 확장 집합 "VMSS001"의 모든 vm 인스턴스에 대 한 롤링 업그레이드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="de35b-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="de35b-111">변수</span><span class="sxs-lookup"><span data-stu-id="de35b-111">PARAMETERS</span></span>

### <span data-ttu-id="de35b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de35b-112">-DefaultProfile</span></span>
<span data-ttu-id="de35b-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="de35b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de35b-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de35b-114">-ResourceGroupName</span></span>
<span data-ttu-id="de35b-115">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="de35b-115">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de35b-116">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="de35b-116">-VMScaleSetName</span></span>
<span data-ttu-id="de35b-117">VM 크기 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="de35b-117">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de35b-118">-확인</span><span class="sxs-lookup"><span data-stu-id="de35b-118">-Confirm</span></span>
<span data-ttu-id="de35b-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="de35b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de35b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de35b-120">-WhatIf</span></span>
<span data-ttu-id="de35b-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="de35b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de35b-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="de35b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de35b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de35b-123">CommonParameters</span></span>
<span data-ttu-id="de35b-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="de35b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de35b-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de35b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de35b-126">입력</span><span class="sxs-lookup"><span data-stu-id="de35b-126">INPUTS</span></span>

### <span data-ttu-id="de35b-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="de35b-127">System.String</span></span>

## <span data-ttu-id="de35b-128">출력</span><span class="sxs-lookup"><span data-stu-id="de35b-128">OUTPUTS</span></span>

### <span data-ttu-id="de35b-129">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="de35b-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="de35b-130">상속자</span><span class="sxs-lookup"><span data-stu-id="de35b-130">NOTES</span></span>

## <span data-ttu-id="de35b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="de35b-131">RELATED LINKS</span></span>

