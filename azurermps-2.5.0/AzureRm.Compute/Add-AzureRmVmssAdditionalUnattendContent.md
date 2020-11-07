---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssadditionalunattendcontent
schema: 2.0.0
ms.openlocfilehash: c0ceb74c6880508f04fb0832c48d0752507f5a5b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881174"
---
# <span data-ttu-id="2621f-101">Add-AzureRmVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="2621f-101">Add-AzureRmVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="2621f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2621f-102">SYNOPSIS</span></span>
<span data-ttu-id="2621f-103">무인 Windows 설치 응답 파일에 정보를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2621f-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2621f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2621f-104">SYNTAX</span></span>

```
Add-AzureRmVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2621f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2621f-105">DESCRIPTION</span></span>
<span data-ttu-id="2621f-106">**추가-AzureRmVmssAdditionalUnattendContent** cmdlet은 정보를 무인 Windows 설치 응답 파일에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2621f-106">The **Add-AzureRmVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="2621f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2621f-107">EXAMPLES</span></span>

### <span data-ttu-id="2621f-108">예제 1: 무인 Windows 설치 응답 파일에 정보 추가</span><span class="sxs-lookup"><span data-stu-id="2621f-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzureRmVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="2621f-109">이 명령은 무인 Windows 설치 응답 파일에 정보를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2621f-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="2621f-110">변수</span><span class="sxs-lookup"><span data-stu-id="2621f-110">PARAMETERS</span></span>

### <span data-ttu-id="2621f-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="2621f-111">-ComponentName</span></span>
<span data-ttu-id="2621f-112">추가 된 콘텐츠를 사용 하 여 구성할 구성 요소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2621f-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="2621f-113">유일 하 게 허용 되는 값은 Microsoft-Windows-셸 설치입니다.</span><span class="sxs-lookup"><span data-stu-id="2621f-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

```yaml
Type: ComponentNames
Parameter Sets: (All)
Aliases: 
Accepted values: MicrosoftWindowsShellSetup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2621f-114">-콘텐츠</span><span class="sxs-lookup"><span data-stu-id="2621f-114">-Content</span></span>
<span data-ttu-id="2621f-115">지정 된 경로와 구성 요소의 unattend.xml 파일에 추가 되는 XML 서식 지정 콘텐츠를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2621f-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2621f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2621f-116">-DefaultProfile</span></span>
<span data-ttu-id="2621f-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2621f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2621f-118">-PassName</span><span class="sxs-lookup"><span data-stu-id="2621f-118">-PassName</span></span>
<span data-ttu-id="2621f-119">콘텐츠가 적용 되는 패스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2621f-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="2621f-120">유일 하 게 허용 되는 값은 oobeSystem입니다.</span><span class="sxs-lookup"><span data-stu-id="2621f-120">The only allowable value is oobeSystem.</span></span>

```yaml
Type: PassNames
Parameter Sets: (All)
Aliases: 
Accepted values: OobeSystem

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2621f-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="2621f-121">-SettingName</span></span>
<span data-ttu-id="2621f-122">콘텐츠가 적용 되는 설정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2621f-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="2621f-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2621f-123">The acceptable values for this parameter are::</span></span>

- <span data-ttu-id="2621f-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="2621f-124">FirstLogonCommands</span></span>
- <span data-ttu-id="2621f-125">자동</span><span class="sxs-lookup"><span data-stu-id="2621f-125">AutoLogon</span></span>

```yaml
Type: SettingNames
Parameter Sets: (All)
Aliases: 
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2621f-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2621f-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="2621f-127">가상 컴퓨터 **크기 집합** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2621f-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="2621f-128">[새 AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2621f-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2621f-129">-확인</span><span class="sxs-lookup"><span data-stu-id="2621f-129">-Confirm</span></span>
<span data-ttu-id="2621f-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2621f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2621f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2621f-131">-WhatIf</span></span>
<span data-ttu-id="2621f-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2621f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2621f-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2621f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2621f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2621f-134">CommonParameters</span></span>
<span data-ttu-id="2621f-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2621f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2621f-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2621f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2621f-137">입력</span><span class="sxs-lookup"><span data-stu-id="2621f-137">INPUTS</span></span>

### <span data-ttu-id="2621f-138">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2621f-138">VirtualMachineScaleSet</span></span>
<span data-ttu-id="2621f-139">' VirtualMachineScaleSet ' 매개 변수는 파이프라인에서 ' VirtualMachineScaleSet ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2621f-139">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="2621f-140">출력</span><span class="sxs-lookup"><span data-stu-id="2621f-140">OUTPUTS</span></span>

### <span data-ttu-id="2621f-141">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="2621f-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="2621f-142">상속자</span><span class="sxs-lookup"><span data-stu-id="2621f-142">NOTES</span></span>

## <span data-ttu-id="2621f-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2621f-143">RELATED LINKS</span></span>

[<span data-ttu-id="2621f-144">새로운 AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="2621f-144">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
