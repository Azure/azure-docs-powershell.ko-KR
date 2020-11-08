---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 455DB2C0-08A0-4D62-B8EE-7C3DB9AD8A8C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85040f07914aef02355f69baab093c75ce7e4afd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045516"
---
# <span data-ttu-id="570b5-101">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="570b5-101">Remove-AzureVM</span></span>

## <span data-ttu-id="570b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="570b5-102">SYNOPSIS</span></span>
<span data-ttu-id="570b5-103">Azure 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="570b5-103">Removes an Azure virtual machine.</span></span>

## <span data-ttu-id="570b5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="570b5-104">SYNTAX</span></span>

```
Remove-AzureVM [-Name] <String> [-DeleteVHD] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="570b5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="570b5-105">DESCRIPTION</span></span>
<span data-ttu-id="570b5-106">**제거-add-azurevm** Cmdlet은 Azure 가상 컴퓨터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="570b5-106">The **Remove-AzureVM** cmdlet deletes an Azure virtual machine.</span></span>
<span data-ttu-id="570b5-107">이 프로세스는 해당 가상 컴퓨터에 탑재 된 디스크의 기본 .vhd 파일을 삭제 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="570b5-107">This process does not delete the underlying .vhd files of the disks mounted on that virtual machine.</span></span>

## <span data-ttu-id="570b5-108">예제의</span><span class="sxs-lookup"><span data-stu-id="570b5-108">EXAMPLES</span></span>

### <span data-ttu-id="570b5-109">예제 1: 서비스에서 가상 컴퓨터 제거</span><span class="sxs-lookup"><span data-stu-id="570b5-109">Example 1: Remove a virtual machine from a service</span></span>
```
PS C:\> Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine03"
```

<span data-ttu-id="570b5-110">이 명령은 ContosoService03 서비스에서 실행 되는 VirtualMachine03 이라는 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="570b5-110">This command removes the virtual machine named VirtualMachine03 that runs in the ContosoService03 service.</span></span>

### <span data-ttu-id="570b5-111">예제 2: 가상 컴퓨터 제거 및 .vhd 파일 삭제</span><span class="sxs-lookup"><span data-stu-id="570b5-111">Example 2: Remove a virtual machine and delete the .vhd files</span></span>
```
PS C:\> Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04" -DeleteVHD
```

<span data-ttu-id="570b5-112">이 명령은 ContosoService03 서비스에서 실행 되는 VirtualMachine04 가상 컴퓨터를 제거 하 고, *Deletevhd* 매개 변수를 사용 하 여 .vhd 파일을 제거 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="570b5-112">This command removes the VirtualMachine04 virtual machine that runs in the ContosoService03 service, and specifies to remove the .vhd files using the *DeleteVHD* parameter.</span></span>

## <span data-ttu-id="570b5-113">변수</span><span class="sxs-lookup"><span data-stu-id="570b5-113">PARAMETERS</span></span>

### <span data-ttu-id="570b5-114">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="570b5-114">-DeleteVHD</span></span>
<span data-ttu-id="570b5-115">이 cmdlet이 가상 컴퓨터 및 기본 디스크 blob을 제거할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="570b5-115">Specifies whether this cmdlet removes the virtual machine and the underlying disk blobs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="570b5-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="570b5-116">-InformationAction</span></span>
<span data-ttu-id="570b5-117">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="570b5-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="570b5-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="570b5-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="570b5-119">하기로</span><span class="sxs-lookup"><span data-stu-id="570b5-119">Continue</span></span>
- <span data-ttu-id="570b5-120">숨기기</span><span class="sxs-lookup"><span data-stu-id="570b5-120">Ignore</span></span>
- <span data-ttu-id="570b5-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="570b5-121">Inquire</span></span>
- <span data-ttu-id="570b5-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="570b5-122">SilentlyContinue</span></span>
- <span data-ttu-id="570b5-123">중지가</span><span class="sxs-lookup"><span data-stu-id="570b5-123">Stop</span></span>
- <span data-ttu-id="570b5-124">대기</span><span class="sxs-lookup"><span data-stu-id="570b5-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="570b5-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="570b5-125">-InformationVariable</span></span>
<span data-ttu-id="570b5-126">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="570b5-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="570b5-127">-이름</span><span class="sxs-lookup"><span data-stu-id="570b5-127">-Name</span></span>
<span data-ttu-id="570b5-128">제거할 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="570b5-128">Specifies the name of the virtual machine being removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="570b5-129">-프로필</span><span class="sxs-lookup"><span data-stu-id="570b5-129">-Profile</span></span>
<span data-ttu-id="570b5-130">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="570b5-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="570b5-131">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="570b5-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="570b5-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="570b5-132">-ServiceName</span></span>
<span data-ttu-id="570b5-133">가상 컴퓨터를 제거할 Azure 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="570b5-133">Specifies the name of the Azure service from which the virtual machine is being removed.</span></span>

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

### <span data-ttu-id="570b5-134">-확인</span><span class="sxs-lookup"><span data-stu-id="570b5-134">-Confirm</span></span>
<span data-ttu-id="570b5-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="570b5-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="570b5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="570b5-136">-WhatIf</span></span>
<span data-ttu-id="570b5-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="570b5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="570b5-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="570b5-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="570b5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="570b5-139">CommonParameters</span></span>
<span data-ttu-id="570b5-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="570b5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="570b5-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="570b5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="570b5-142">입력</span><span class="sxs-lookup"><span data-stu-id="570b5-142">INPUTS</span></span>

## <span data-ttu-id="570b5-143">출력</span><span class="sxs-lookup"><span data-stu-id="570b5-143">OUTPUTS</span></span>

## <span data-ttu-id="570b5-144">상속자</span><span class="sxs-lookup"><span data-stu-id="570b5-144">NOTES</span></span>

## <span data-ttu-id="570b5-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="570b5-145">RELATED LINKS</span></span>

[<span data-ttu-id="570b5-146">뉴욕</span><span class="sxs-lookup"><span data-stu-id="570b5-146">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="570b5-147">새로운 AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="570b5-147">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="570b5-148">-Add-azurevm 다시 시작</span><span class="sxs-lookup"><span data-stu-id="570b5-148">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="570b5-149">시작-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="570b5-149">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="570b5-150">-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="570b5-150">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="570b5-151">업데이트-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="570b5-151">Update-AzureVM</span></span>](./Update-AzureVM.md)


