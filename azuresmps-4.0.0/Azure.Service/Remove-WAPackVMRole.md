---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9999E0EE-4A32-4C18-A6EC-2A073DC08710
online version: ''
schema: 2.0.0
ms.openlocfilehash: e5dfe0f42987ba51613ff9bafa000713456dfaf7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047411"
---
# <span data-ttu-id="189fc-101">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="189fc-101">Remove-WAPackVMRole</span></span>

## <span data-ttu-id="189fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="189fc-102">SYNOPSIS</span></span>
<span data-ttu-id="189fc-103">가상 컴퓨터 역할 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-103">Removes virtual machine role objects.</span></span>

## <span data-ttu-id="189fc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="189fc-104">SYNTAX</span></span>

### <span data-ttu-id="189fc-105">FromVMRoleObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="189fc-105">FromVMRoleObject (Default)</span></span>
```
Remove-WAPackVMRole -VMRole <VMRole> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="189fc-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="189fc-106">FromCloudService</span></span>
```
Remove-WAPackVMRole -VMRole <VMRole> -CloudServiceName <String> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="189fc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="189fc-107">DESCRIPTION</span></span>
<span data-ttu-id="189fc-108">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="189fc-109">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="189fc-110">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="189fc-111">**WAPackVMRole** cmdlet은 가상 컴퓨터 역할 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-111">The **Remove-WAPackVMRole** cmdlet removes virtual machine role objects.</span></span>

## <span data-ttu-id="189fc-112">예제의</span><span class="sxs-lookup"><span data-stu-id="189fc-112">EXAMPLES</span></span>

### <span data-ttu-id="189fc-113">예제 1: WAP 포털을 사용 하 여 만든 가상 컴퓨터 역할 제거</span><span class="sxs-lookup"><span data-stu-id="189fc-113">Example 1: Remove a virtual machine role (which was created using the WAP portal)</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole
```

<span data-ttu-id="189fc-114">첫 번째 명령은 **WAPackVMRole** cmdlet을 사용 하 여 ContosoVMRole01 이라는 가상 컴퓨터 역할을 가져온 다음 해당 개체를 $VMRole 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-114">The first command gets the virtual machine role named ContosoVMRole01 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="189fc-115">두 번째 명령은 $VMRole에 저장 된 가상 컴퓨터 역할을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-115">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="189fc-116">명령에서 확인 하 라는 메시지를 표시 합니다. 이 가상 컴퓨터 역할을 WAP 포털을 사용 하 여 만든 것으로 가정 하면 클라우드 서비스 이름을 지정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-116">The command prompts you for confirmation.Assuming this virtual machine role was created using the WAP portal, there's no need to specify the cloud service name.</span></span>

### <span data-ttu-id="189fc-117">예제 2: 클라우드 서비스를 수동으로 만든 후 생성 된 가상 컴퓨터 역할 제거</span><span class="sxs-lookup"><span data-stu-id="189fc-117">Example 2: Remove a virtual machine role which was created after manually creating a cloud service</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole02"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -CloudServiceName "ContosoCloudService02"
```

<span data-ttu-id="189fc-118">첫 번째 명령은 **WAPackVMRole** cmdlet을 사용 하 여 "ContosoVMRole02" 라는 가상 컴퓨터 역할을 가져온 다음 해당 개체를 $VMRole 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-118">The first command gets the virtual machine role named "ContosoVMRole02" by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="189fc-119">두 번째 명령은 $VMRole에 저장 된 가상 컴퓨터 역할을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-119">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="189fc-120">명령에서 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="189fc-121">포털을 사용 하 여이 가상 컴퓨터 역할이 만들어지지 않았다고 가정할 경우 사용자는 클라우드 서비스 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-121">Assuming this virtual machine role was not created using the portal, the user needs to specify the cloud service name.</span></span>
<span data-ttu-id="189fc-122">이 경우에는 "ContosoCloudService02"입니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-122">In this case named "ContosoCloudService02".</span></span>

### <span data-ttu-id="189fc-123">예제 3: 확인 하지 않고 가상 컴퓨터 역할 제거</span><span class="sxs-lookup"><span data-stu-id="189fc-123">Example 3: Remove a virtual machine role without confirmation</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole03"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -Force
```

<span data-ttu-id="189fc-124">첫 번째 명령은 **WAPackVMRole** cmdlet을 사용 하 여 ContosoVMRole03 이라는 클라우드 서비스를 가져온 다음 해당 개체를 $VMRole 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-124">The first command gets the cloud service named ContosoVMRole03 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="189fc-125">두 번째 명령은 $VMRole에 저장 된 가상 컴퓨터 역할을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-125">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="189fc-126">이 명령에는 *Force* 매개 변수가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-126">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="189fc-127">명령에 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-127">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="189fc-128">변수</span><span class="sxs-lookup"><span data-stu-id="189fc-128">PARAMETERS</span></span>

### <span data-ttu-id="189fc-129">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="189fc-129">-CloudServiceName</span></span>
<span data-ttu-id="189fc-130">가상 컴퓨터 역할의 클라우드 서비스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-130">Specifies the cloud service name of virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="189fc-131">-Force</span><span class="sxs-lookup"><span data-stu-id="189fc-131">-Force</span></span>
<span data-ttu-id="189fc-132">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="189fc-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="189fc-133">-PassThru</span></span>
<span data-ttu-id="189fc-134">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-134">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="189fc-135">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-135">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="189fc-136">-프로필</span><span class="sxs-lookup"><span data-stu-id="189fc-136">-Profile</span></span>
<span data-ttu-id="189fc-137">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="189fc-138">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="189fc-139">-VMRole</span><span class="sxs-lookup"><span data-stu-id="189fc-139">-VMRole</span></span>
<span data-ttu-id="189fc-140">가상 컴퓨터 역할을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-140">Specifies a virtual machine role.</span></span>
<span data-ttu-id="189fc-141">가상 컴퓨터 역할을 얻으려면 **get-WAPackVMRole** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-141">To get a virtual machine role, use the **Get-WAPackVMRole** cmdlet.</span></span>

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="189fc-142">-확인</span><span class="sxs-lookup"><span data-stu-id="189fc-142">-Confirm</span></span>
<span data-ttu-id="189fc-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="189fc-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="189fc-144">-WhatIf</span></span>
<span data-ttu-id="189fc-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="189fc-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="189fc-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="189fc-147">CommonParameters</span></span>
<span data-ttu-id="189fc-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="189fc-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="189fc-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="189fc-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="189fc-150">입력</span><span class="sxs-lookup"><span data-stu-id="189fc-150">INPUTS</span></span>

## <span data-ttu-id="189fc-151">출력</span><span class="sxs-lookup"><span data-stu-id="189fc-151">OUTPUTS</span></span>

## <span data-ttu-id="189fc-152">상속자</span><span class="sxs-lookup"><span data-stu-id="189fc-152">NOTES</span></span>

## <span data-ttu-id="189fc-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="189fc-153">RELATED LINKS</span></span>

[<span data-ttu-id="189fc-154">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="189fc-154">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="189fc-155">새로운 WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="189fc-155">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="189fc-156">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="189fc-156">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


