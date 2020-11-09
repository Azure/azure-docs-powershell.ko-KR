---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
ms.openlocfilehash: c6af342183b7f1b2aa9bf7695ba8486ec193698a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308522"
---
# <span data-ttu-id="d462f-101">New-AzVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="d462f-101">New-AzVmssIpTagConfig</span></span>

## <span data-ttu-id="d462f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d462f-102">SYNOPSIS</span></span>
<span data-ttu-id="d462f-103">VMSS의 네트워크 인터페이스에 대 한 IP 태그 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d462f-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

## <span data-ttu-id="d462f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d462f-104">SYNTAX</span></span>

```
New-AzVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d462f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d462f-105">DESCRIPTION</span></span>
<span data-ttu-id="d462f-106">**AzVmssIpTagConfig** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)의 네트워크 인터페이스에 대 한 IP 태그 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d462f-106">The **New-AzVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="d462f-107">이 cmdlet의 구성을 New-AzVmssIpConfig cmdlet의 *Iptag* 매개 변수로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d462f-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="d462f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="d462f-108">EXAMPLES</span></span>

### <span data-ttu-id="d462f-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="d462f-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="d462f-110">이 명령은 ' FirstPartyUsage ' 형식 및 ' Sql ' 태그를 사용 하 여 IP 태그 로컬 개체를 만든 다음이 IP 태그를 사용 하 여 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d462f-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="d462f-111">변수</span><span class="sxs-lookup"><span data-stu-id="d462f-111">PARAMETERS</span></span>

### <span data-ttu-id="d462f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d462f-112">-DefaultProfile</span></span>
<span data-ttu-id="d462f-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d462f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d462f-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="d462f-114">-IpTagType</span></span>
<span data-ttu-id="d462f-115">IP 태그 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d462f-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="d462f-116">태그</span><span class="sxs-lookup"><span data-stu-id="d462f-116">-Tag</span></span>
<span data-ttu-id="d462f-117">IP 태그 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d462f-117">Specifies an IP Tag Value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d462f-118">-확인</span><span class="sxs-lookup"><span data-stu-id="d462f-118">-Confirm</span></span>
<span data-ttu-id="d462f-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d462f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d462f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d462f-120">-WhatIf</span></span>
<span data-ttu-id="d462f-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d462f-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d462f-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d462f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d462f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d462f-123">CommonParameters</span></span>
<span data-ttu-id="d462f-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d462f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d462f-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d462f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d462f-126">입력</span><span class="sxs-lookup"><span data-stu-id="d462f-126">INPUTS</span></span>

### <span data-ttu-id="d462f-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d462f-127">System.String</span></span>

## <span data-ttu-id="d462f-128">출력</span><span class="sxs-lookup"><span data-stu-id="d462f-128">OUTPUTS</span></span>

### <span data-ttu-id="d462f-129">VirtualMachineScaleSetIpTag를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="d462f-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="d462f-130">상속자</span><span class="sxs-lookup"><span data-stu-id="d462f-130">NOTES</span></span>

## <span data-ttu-id="d462f-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d462f-131">RELATED LINKS</span></span>
