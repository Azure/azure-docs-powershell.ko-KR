---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/disable-azurermvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
ms.openlocfilehash: 7ff2512fa7c6247d75eb8b288c888dc2aff670dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530563"
---
# <span data-ttu-id="ab8ab-101">Disable-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="ab8ab-101">Disable-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="ab8ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab8ab-102">SYNOPSIS</span></span>
<span data-ttu-id="ab8ab-103">VM 크기 집합에서 디스크 암호화를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8ab-103">Disables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab8ab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab8ab-104">SYNTAX</span></span>

```
Disable-AzureRmVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab8ab-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ab8ab-105">DESCRIPTION</span></span>
<span data-ttu-id="ab8ab-106">VM 크기 집합에서 디스크 암호화를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8ab-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="ab8ab-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ab8ab-107">EXAMPLES</span></span>

### <span data-ttu-id="ab8ab-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ab8ab-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="ab8ab-109">Group001 이라는 리소스 그룹에 속하는 VMSS001 이라는 VM 크기 집합에서 디스크 암호화를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8ab-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="ab8ab-110">변수</span><span class="sxs-lookup"><span data-stu-id="ab8ab-110">PARAMETERS</span></span>

### <span data-ttu-id="ab8ab-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab8ab-111">-AsJob</span></span>
<span data-ttu-id="ab8ab-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ab8ab-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab8ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab8ab-113">-DefaultProfile</span></span>
<span data-ttu-id="ab8ab-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab8ab-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab8ab-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="ab8ab-115">-ExtensionName</span></span>
<span data-ttu-id="ab8ab-116">확장명 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab8ab-116">The extension name.</span></span>
<span data-ttu-id="ab8ab-117">이 매개 변수를 지정 하지 않으면 windows Vm 용 azurediskencryption 용 AzureDiskEncryption를 사용 하 여 기본 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab8ab-117">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8ab-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ab8ab-118">-Force</span></span>
<span data-ttu-id="ab8ab-119">가상 컴퓨터에서 확장을 강제로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8ab-119">To force the removal of the extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab8ab-120">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="ab8ab-120">-ForceUpdate</span></span>
<span data-ttu-id="ab8ab-121">강제 업데이트에 대 한 태그를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8ab-121">Generate a tag for force update.</span></span>  <span data-ttu-id="ab8ab-122">동일한 VM에서 반복 되는 암호화 작업을 수행 하도록 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8ab-122">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8ab-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab8ab-123">-ResourceGroupName</span></span>
<span data-ttu-id="ab8ab-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab8ab-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8ab-125">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ab8ab-125">-VMScaleSetName</span></span>
<span data-ttu-id="ab8ab-126">가상 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab8ab-126">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8ab-127">-가이 Etype</span><span class="sxs-lookup"><span data-stu-id="ab8ab-127">-VolumeType</span></span>
<span data-ttu-id="ab8ab-128">암호화 작업을 수행할 볼륨 유형 (OS 또는 데이터)</span><span class="sxs-lookup"><span data-stu-id="ab8ab-128">Type of the volume (OS or Data) to perform encryption operation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8ab-129">-확인</span><span class="sxs-lookup"><span data-stu-id="ab8ab-129">-Confirm</span></span>
<span data-ttu-id="ab8ab-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8ab-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab8ab-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab8ab-131">-WhatIf</span></span>
<span data-ttu-id="ab8ab-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ab8ab-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab8ab-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab8ab-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab8ab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab8ab-134">CommonParameters</span></span>
<span data-ttu-id="ab8ab-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8ab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab8ab-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab8ab-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab8ab-137">입력</span><span class="sxs-lookup"><span data-stu-id="ab8ab-137">INPUTS</span></span>

### <span data-ttu-id="ab8ab-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ab8ab-138">System.String</span></span>

## <span data-ttu-id="ab8ab-139">출력</span><span class="sxs-lookup"><span data-stu-id="ab8ab-139">OUTPUTS</span></span>

### <span data-ttu-id="ab8ab-140">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="ab8ab-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ab8ab-141">상속자</span><span class="sxs-lookup"><span data-stu-id="ab8ab-141">NOTES</span></span>

## <span data-ttu-id="ab8ab-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab8ab-142">RELATED LINKS</span></span>
