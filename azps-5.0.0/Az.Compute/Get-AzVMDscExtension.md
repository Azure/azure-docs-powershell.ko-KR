---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: ba4ac8d48c72ffac164e447777670c48f529f68f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216416"
---
# <span data-ttu-id="418fe-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="418fe-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="418fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="418fe-102">SYNOPSIS</span></span>
<span data-ttu-id="418fe-103">특정 가상 컴퓨터에서 DSC 확장의 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="418fe-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="418fe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="418fe-104">SYNTAX</span></span>

```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="418fe-105">설명은</span><span class="sxs-lookup"><span data-stu-id="418fe-105">DESCRIPTION</span></span>
<span data-ttu-id="418fe-106">**AzVMDscExtension** cmdlet은 특정 가상 컴퓨터에서 DSC (원하는 상태 구성) 확장의 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="418fe-106">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="418fe-107">예제의</span><span class="sxs-lookup"><span data-stu-id="418fe-107">EXAMPLES</span></span>

### <span data-ttu-id="418fe-108">예제 1: DSC 확장의 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="418fe-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="418fe-109">이 명령은 VM07 이라는 가상 컴퓨터에서 DSC 라는 확장의 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="418fe-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="418fe-110">변수</span><span class="sxs-lookup"><span data-stu-id="418fe-110">PARAMETERS</span></span>

### <span data-ttu-id="418fe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="418fe-111">-DefaultProfile</span></span>
<span data-ttu-id="418fe-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="418fe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="418fe-113">-이름</span><span class="sxs-lookup"><span data-stu-id="418fe-113">-Name</span></span>
<span data-ttu-id="418fe-114">확장을 나타내는 Azure Resource Manager 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="418fe-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="418fe-115">Set-AzVMDscExtension cmdlet은이 이름을 **AzVMDscExtension** 에서 사용 하는 것과 동일한 값인 Microsoft Powershell로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="418fe-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="418fe-116">**AzVMDscExtension** cmdlet에서 기본 이름을 변경 하거나 리소스 관리자 템플릿에서 다른 리소스 이름을 사용 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="418fe-116">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="418fe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="418fe-117">-ResourceGroupName</span></span>
<span data-ttu-id="418fe-118">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="418fe-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="418fe-119">-상태</span><span class="sxs-lookup"><span data-stu-id="418fe-119">-Status</span></span>
<span data-ttu-id="418fe-120">이 cmdlet이 DSC 확장의 인스턴스 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="418fe-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="418fe-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="418fe-121">-VMName</span></span>
<span data-ttu-id="418fe-122">이 cmdlet이 DSC 확장을 가져오는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="418fe-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="418fe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="418fe-123">CommonParameters</span></span>
<span data-ttu-id="418fe-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="418fe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="418fe-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="418fe-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="418fe-126">입력</span><span class="sxs-lookup"><span data-stu-id="418fe-126">INPUTS</span></span>

### <span data-ttu-id="418fe-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="418fe-127">System.String</span></span>

### <span data-ttu-id="418fe-128">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="418fe-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="418fe-129">출력</span><span class="sxs-lookup"><span data-stu-id="418fe-129">OUTPUTS</span></span>

### <span data-ttu-id="418fe-130">VirtualMachineDscExtensionContext. 확장명은. m m.</span><span class="sxs-lookup"><span data-stu-id="418fe-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="418fe-131">상속자</span><span class="sxs-lookup"><span data-stu-id="418fe-131">NOTES</span></span>

## <span data-ttu-id="418fe-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="418fe-132">RELATED LINKS</span></span>

[<span data-ttu-id="418fe-133">제거-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="418fe-133">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="418fe-134">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="418fe-134">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


