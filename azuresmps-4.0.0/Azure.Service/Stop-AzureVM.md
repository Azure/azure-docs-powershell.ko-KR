---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4F347DD1-907C-47DB-8F1D-636DE031A56A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e01265cf3db8a0dc3fd9d74a4a263a20965b10fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045741"
---
# <span data-ttu-id="02b6c-101">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="02b6c-101">Stop-AzureVM</span></span>

## <span data-ttu-id="02b6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="02b6c-103">Azure 가상 컴퓨터를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b6c-103">Shuts down an Azure virtual machine.</span></span>

## <span data-ttu-id="02b6c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02b6c-104">SYNTAX</span></span>

### <span data-ttu-id="02b6c-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="02b6c-105">ByName (Default)</span></span>
```
Stop-AzureVM [-Name] <String[]> [-StayProvisioned] [-Force] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="02b6c-106">의견</span><span class="sxs-lookup"><span data-stu-id="02b6c-106">Input</span></span>
```
Stop-AzureVM -VM <IPersistentVM[]> [-StayProvisioned] [-Force] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="02b6c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="02b6c-107">DESCRIPTION</span></span>
<span data-ttu-id="02b6c-108">이 **(가) add-azurevm** cmdlet이 가상 컴퓨터를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b6c-108">The **Stop-AzureVM** cmdlet shuts down a virtual machine.</span></span>

## <span data-ttu-id="02b6c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="02b6c-109">EXAMPLES</span></span>

### <span data-ttu-id="02b6c-110">예제 1: 가상 컴퓨터 종료</span><span class="sxs-lookup"><span data-stu-id="02b6c-110">Example 1: Shut down a virtual machine</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM"
```

<span data-ttu-id="02b6c-111">이 명령은 지정 된 서비스가 포함 하는 가상 컴퓨터를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b6c-111">This command shuts down a virtual machine that the specified service contains.</span></span>

### <span data-ttu-id="02b6c-112">예제 2: 가상 컴퓨터 개체를 사용 하 여 가상 컴퓨터 종료</span><span class="sxs-lookup"><span data-stu-id="02b6c-112">Example 2: Shut down a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "MyVM" | Stop-AzureVM
```

<span data-ttu-id="02b6c-113">이 명령은 지정 된 서비스가 포함 하는 가상 컴퓨터를 종료 하는 데 사용 되는 가상 컴퓨터 개체를 통해 **시작** 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b6c-113">This command shuts down a virtual machine that the specified service contains, by using the virtual machine object that **Get-AzureVM** returns.</span></span>

### <span data-ttu-id="02b6c-114">예제 3: VM을 종료 하 고 VM을 프로 비전 된 상태로 유지</span><span class="sxs-lookup"><span data-stu-id="02b6c-114">Example 3: Shut down a VM and keep the VM provisioned</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -StayProvisioned
```

<span data-ttu-id="02b6c-115">이 명령은 지정 된 서비스에 포함 되어 있는 가상 컴퓨터를 종료 하 고 계속 프로 비전 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b6c-115">This command shuts down a virtual machine that the specified service contains, and keeps it provisioned.</span></span>

### <span data-ttu-id="02b6c-116">예제 4: VM 종료 및 배포에서 마지막 VM의 할당 취소 허용</span><span class="sxs-lookup"><span data-stu-id="02b6c-116">Example 4: Shut down a VM and allow deallocation of the last VM in the deployment</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -Force
```

<span data-ttu-id="02b6c-117">이 명령은 지정 된 서비스가 포함 하는 가상 컴퓨터를 종료 하 고 배포의 마지막 가상 컴퓨터에 대 한 할당 취소를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b6c-117">This command shuts down a virtual machine that the specified service contains and allows deallocation of the last virtual machine in the deployment.</span></span>

### <span data-ttu-id="02b6c-118">예제 5: 여러 Vm 종료</span><span class="sxs-lookup"><span data-stu-id="02b6c-118">Example 5: Shut down multiple VMs</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "PSTestService" -Name "*" -Force
```

<span data-ttu-id="02b6c-119">이 명령은 지정 된 서비스에 포함 되어 있는 여러 가상 컴퓨터를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b6c-119">This command shuts down multiple virtual machines that the specified service contains.</span></span>

## <span data-ttu-id="02b6c-120">변수</span><span class="sxs-lookup"><span data-stu-id="02b6c-120">PARAMETERS</span></span>

### <span data-ttu-id="02b6c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="02b6c-121">-Force</span></span>
<span data-ttu-id="02b6c-122">배포에서 마지막 가상 컴퓨터의 할당 취소를 허용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b6c-122">Specifies whether to allow the deallocation of the last virtual machine in a deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b6c-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="02b6c-123">-InformationAction</span></span>
<span data-ttu-id="02b6c-124">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b6c-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="02b6c-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="02b6c-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="02b6c-126">하기로</span><span class="sxs-lookup"><span data-stu-id="02b6c-126">Continue</span></span>
- <span data-ttu-id="02b6c-127">숨기기</span><span class="sxs-lookup"><span data-stu-id="02b6c-127">Ignore</span></span>
- <span data-ttu-id="02b6c-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="02b6c-128">Inquire</span></span>
- <span data-ttu-id="02b6c-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="02b6c-129">SilentlyContinue</span></span>
- <span data-ttu-id="02b6c-130">중지가</span><span class="sxs-lookup"><span data-stu-id="02b6c-130">Stop</span></span>
- <span data-ttu-id="02b6c-131">대기</span><span class="sxs-lookup"><span data-stu-id="02b6c-131">Suspend</span></span>

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

### <span data-ttu-id="02b6c-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="02b6c-132">-InformationVariable</span></span>
<span data-ttu-id="02b6c-133">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b6c-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="02b6c-134">-이름</span><span class="sxs-lookup"><span data-stu-id="02b6c-134">-Name</span></span>
<span data-ttu-id="02b6c-135">종료할 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b6c-135">Specifies the name of the virtual machine to shut down.</span></span>

<span data-ttu-id="02b6c-136">와일드 카드 문자를 사용 하 여 여러 가상 컴퓨터를 비동기적으로 중지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="02b6c-136">Use the wildcard character to stop multiple virtual machines asynchronously.</span></span>
<span data-ttu-id="02b6c-137">와일드 카드 문자를 사용 하는 경우이 cmdlet은 종료 역할 작업 https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx) https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx) .</span><span class="sxs-lookup"><span data-stu-id="02b6c-137">With a wildcard character, this cmdlet calls the Shutdown Roleshttps://msdn.microsoft.com/en-us/library/azure/dn469421.aspx operation (https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx), instead of the Shutdown Rolehttps://msdn.microsoft.com/en-us/library/azure/jj157195.aspx operation (https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx).</span></span>

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02b6c-138">-프로필</span><span class="sxs-lookup"><span data-stu-id="02b6c-138">-Profile</span></span>
<span data-ttu-id="02b6c-139">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b6c-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="02b6c-140">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="02b6c-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="02b6c-141">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="02b6c-141">-ServiceName</span></span>
<span data-ttu-id="02b6c-142">종료할 가상 컴퓨터를 포함 하는 Azure 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b6c-142">Specifies the name of the Azure service that contains the virtual machine to shut down.</span></span>

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

### <span data-ttu-id="02b6c-143">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="02b6c-143">-StayProvisioned</span></span>
<span data-ttu-id="02b6c-144">이 cmdlet이 가상 컴퓨터를 프로 비전 된 상태로 유지 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b6c-144">Specifies that this cmdlet keeps the virtual machine provisioned.</span></span>

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

### <span data-ttu-id="02b6c-145">-VM</span><span class="sxs-lookup"><span data-stu-id="02b6c-145">-VM</span></span>
<span data-ttu-id="02b6c-146">종료할 가상 컴퓨터를 식별 하는 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b6c-146">Specifies a virtual machine object that identifies the virtual machine to shut down.</span></span>

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02b6c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02b6c-147">CommonParameters</span></span>
<span data-ttu-id="02b6c-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b6c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02b6c-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02b6c-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02b6c-150">입력</span><span class="sxs-lookup"><span data-stu-id="02b6c-150">INPUTS</span></span>

## <span data-ttu-id="02b6c-151">출력</span><span class="sxs-lookup"><span data-stu-id="02b6c-151">OUTPUTS</span></span>

## <span data-ttu-id="02b6c-152">상속자</span><span class="sxs-lookup"><span data-stu-id="02b6c-152">NOTES</span></span>

## <span data-ttu-id="02b6c-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02b6c-153">RELATED LINKS</span></span>

[<span data-ttu-id="02b6c-154">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="02b6c-154">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="02b6c-155">뉴욕</span><span class="sxs-lookup"><span data-stu-id="02b6c-155">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="02b6c-156">-Add-azurevm 다시 시작</span><span class="sxs-lookup"><span data-stu-id="02b6c-156">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="02b6c-157">시작-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="02b6c-157">Start-AzureVM</span></span>](./Start-AzureVM.md)


