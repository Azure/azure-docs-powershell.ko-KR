---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 6ed6176b0f30a754156d2ce03ed0d5acad6e48f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216582"
---
# <span data-ttu-id="ba0fa-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ba0fa-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="ba0fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba0fa-102">SYNOPSIS</span></span>
<span data-ttu-id="ba0fa-103">가상 머신에서 AEM 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba0fa-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="ba0fa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ba0fa-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba0fa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ba0fa-105">DESCRIPTION</span></span>
<span data-ttu-id="ba0fa-106">**AzVMAEMExtension** cmdlet은 가상 머신에서 Azure 확장 모니터링 (AEM) 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba0fa-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="ba0fa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ba0fa-107">EXAMPLES</span></span>

### <span data-ttu-id="ba0fa-108">예제 1: AEM 확장 제거</span><span class="sxs-lookup"><span data-stu-id="ba0fa-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="ba0fa-109">이 명령은 contoso-server 라는 가상 컴퓨터에 대 한 AEM 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba0fa-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="ba0fa-110">변수</span><span class="sxs-lookup"><span data-stu-id="ba0fa-110">PARAMETERS</span></span>

### <span data-ttu-id="ba0fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba0fa-111">-DefaultProfile</span></span>
<span data-ttu-id="ba0fa-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba0fa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba0fa-113">-이름</span><span class="sxs-lookup"><span data-stu-id="ba0fa-113">-Name</span></span>
<span data-ttu-id="ba0fa-114">이 cmdlet이 AEM 확장명을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba0fa-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba0fa-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ba0fa-115">-NoWait</span></span>
<span data-ttu-id="ba0fa-116">작업이 완료 되기 전에 작업을 시작 하 고 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba0fa-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ba0fa-117">작업이 성공적으로 완료 되었는지 확인 하려면 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba0fa-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="ba0fa-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="ba0fa-118">-OSType</span></span>
<span data-ttu-id="ba0fa-119">운영 체제 디스크의 운영 체제 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba0fa-119">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="ba0fa-120">운영 체제 디스크에 형식이 없는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba0fa-120">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="ba0fa-121">이 매개 변수에 허용 되는 값은 Windows 및 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="ba0fa-121">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba0fa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba0fa-122">-ResourceGroupName</span></span>
<span data-ttu-id="ba0fa-123">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba0fa-123">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="ba0fa-124">이 cmdlet은 해당 가상 컴퓨터에서 AEM 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba0fa-124">This cmdlet removes the AEM extension from that virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba0fa-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="ba0fa-125">-VMName</span></span>
<span data-ttu-id="ba0fa-126">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba0fa-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ba0fa-127">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 AEM 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba0fa-127">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba0fa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba0fa-128">CommonParameters</span></span>
<span data-ttu-id="ba0fa-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba0fa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba0fa-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ba0fa-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba0fa-131">입력</span><span class="sxs-lookup"><span data-stu-id="ba0fa-131">INPUTS</span></span>

### <span data-ttu-id="ba0fa-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ba0fa-132">System.String</span></span>

## <span data-ttu-id="ba0fa-133">출력</span><span class="sxs-lookup"><span data-stu-id="ba0fa-133">OUTPUTS</span></span>

### <span data-ttu-id="ba0fa-134">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="ba0fa-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ba0fa-135">상속자</span><span class="sxs-lookup"><span data-stu-id="ba0fa-135">NOTES</span></span>

## <span data-ttu-id="ba0fa-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba0fa-136">RELATED LINKS</span></span>

[<span data-ttu-id="ba0fa-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ba0fa-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="ba0fa-138">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ba0fa-138">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="ba0fa-139">테스트-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="ba0fa-139">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


