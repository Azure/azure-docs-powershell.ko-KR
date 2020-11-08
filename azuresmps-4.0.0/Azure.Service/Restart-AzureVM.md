---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 596B8A6F-D3C2-4170-BCD7-B7A1CDB656D8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ee767e1ba4c5008837e7cef98aafa4017465829
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046073"
---
# <span data-ttu-id="1936a-101">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="1936a-101">Restart-AzureVM</span></span>

## <span data-ttu-id="1936a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1936a-102">SYNOPSIS</span></span>
<span data-ttu-id="1936a-103">Azure 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1936a-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="1936a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1936a-104">SYNTAX</span></span>

### <span data-ttu-id="1936a-105">RestartByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="1936a-105">RestartByName (Default)</span></span>
```
Restart-AzureVM [-Name] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1936a-106">RedeployByName</span><span class="sxs-lookup"><span data-stu-id="1936a-106">RedeployByName</span></span>
```
Restart-AzureVM [-Name] <String> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1936a-107">InitiateMaintenanceByName</span><span class="sxs-lookup"><span data-stu-id="1936a-107">InitiateMaintenanceByName</span></span>
```
Restart-AzureVM [-Name] <String> [-InitiateMaintenance] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1936a-108">RestartInput</span><span class="sxs-lookup"><span data-stu-id="1936a-108">RestartInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1936a-109">RedeployInput</span><span class="sxs-lookup"><span data-stu-id="1936a-109">RedeployInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1936a-110">InitiateMaintenanceInput</span><span class="sxs-lookup"><span data-stu-id="1936a-110">InitiateMaintenanceInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-InitiateMaintenance] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1936a-111">설명은</span><span class="sxs-lookup"><span data-stu-id="1936a-111">DESCRIPTION</span></span>
<span data-ttu-id="1936a-112">**Add-azurevm** Cmdlet은 Azure 가상 컴퓨터의 다시 시작을 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="1936a-112">The **Restart-AzureVM** cmdlet requests a restart of an Azure virtual machine.</span></span>

## <span data-ttu-id="1936a-113">예제의</span><span class="sxs-lookup"><span data-stu-id="1936a-113">EXAMPLES</span></span>

### <span data-ttu-id="1936a-114">예제 1: 가상 컴퓨터 다시 시작</span><span class="sxs-lookup"><span data-stu-id="1936a-114">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureVM -ServiceName "MyService01" -Name "MyVM"
```

<span data-ttu-id="1936a-115">이 명령은 Service01 이라는 Azure 서비스에서 실행 되는 VirtualMachine27 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1936a-115">This command restarts the VirtualMachine27 virtual machine running in the Azure service named Service01.</span></span>

### <span data-ttu-id="1936a-116">예제 2: 가상 컴퓨터 개체를 사용 하 여 가상 컴퓨터 다시 시작</span><span class="sxs-lookup"><span data-stu-id="1936a-116">Example 2: Restart a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "MyService01" -Name "VirtualMachine27" | Restart-AzureVM
```

<span data-ttu-id="1936a-117">이 명령은 MyVM 이라는 가상 컴퓨터에 대 한 가상 컴퓨터 개체를 검색 한 다음 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1936a-117">This command retrieves the virtual machine object for the virtual machine named MyVM and then restarts it.</span></span>

## <span data-ttu-id="1936a-118">변수</span><span class="sxs-lookup"><span data-stu-id="1936a-118">PARAMETERS</span></span>

### <span data-ttu-id="1936a-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1936a-119">-InformationAction</span></span>
<span data-ttu-id="1936a-120">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1936a-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1936a-121">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1936a-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1936a-122">하기로</span><span class="sxs-lookup"><span data-stu-id="1936a-122">Continue</span></span>
- <span data-ttu-id="1936a-123">숨기기</span><span class="sxs-lookup"><span data-stu-id="1936a-123">Ignore</span></span>
- <span data-ttu-id="1936a-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="1936a-124">Inquire</span></span>
- <span data-ttu-id="1936a-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1936a-125">SilentlyContinue</span></span>
- <span data-ttu-id="1936a-126">중지가</span><span class="sxs-lookup"><span data-stu-id="1936a-126">Stop</span></span>
- <span data-ttu-id="1936a-127">대기</span><span class="sxs-lookup"><span data-stu-id="1936a-127">Suspend</span></span>

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

### <span data-ttu-id="1936a-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1936a-128">-InformationVariable</span></span>
<span data-ttu-id="1936a-129">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1936a-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1936a-130">-InitiateMaintenance</span><span class="sxs-lookup"><span data-stu-id="1936a-130">-InitiateMaintenance</span></span>
<span data-ttu-id="1936a-131">가상 머신에서 유지 관리 시작</span><span class="sxs-lookup"><span data-stu-id="1936a-131">Initiate Maintenance on the Virtual Machine</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: InitiateMaintenanceByName, InitiateMaintenanceInput
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1936a-132">-이름</span><span class="sxs-lookup"><span data-stu-id="1936a-132">-Name</span></span>
<span data-ttu-id="1936a-133">다시 시작할 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1936a-133">Specifies the name of the virtual machine to restart.</span></span>

```yaml
Type: String
Parameter Sets: RestartByName, RedeployByName, InitiateMaintenanceByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1936a-134">-프로필</span><span class="sxs-lookup"><span data-stu-id="1936a-134">-Profile</span></span>
<span data-ttu-id="1936a-135">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1936a-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1936a-136">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="1936a-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1936a-137">-재배포</span><span class="sxs-lookup"><span data-stu-id="1936a-137">-Redeploy</span></span>
<span data-ttu-id="1936a-138">Cmdlet이 가상 컴퓨터를 다시 배포 한다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1936a-138">Indicates that the cmdlet redeploys the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RedeployByName, RedeployInput
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1936a-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1936a-139">-ServiceName</span></span>
<span data-ttu-id="1936a-140">다시 시작할 가상 컴퓨터를 포함 하는 Azure 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1936a-140">Specifies the name of the Azure service that contains the virtual machine to restart.</span></span>

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

### <span data-ttu-id="1936a-141">-VM</span><span class="sxs-lookup"><span data-stu-id="1936a-141">-VM</span></span>
<span data-ttu-id="1936a-142">다시 시작할 가상 컴퓨터를 식별 하는 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1936a-142">Specifies a virtual machine object that identifies the virtual machine to restart.</span></span>

```yaml
Type: PersistentVM
Parameter Sets: RestartInput, RedeployInput, InitiateMaintenanceInput
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1936a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1936a-143">CommonParameters</span></span>
<span data-ttu-id="1936a-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1936a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1936a-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1936a-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1936a-146">입력</span><span class="sxs-lookup"><span data-stu-id="1936a-146">INPUTS</span></span>

## <span data-ttu-id="1936a-147">출력</span><span class="sxs-lookup"><span data-stu-id="1936a-147">OUTPUTS</span></span>

## <span data-ttu-id="1936a-148">상속자</span><span class="sxs-lookup"><span data-stu-id="1936a-148">NOTES</span></span>

## <span data-ttu-id="1936a-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1936a-149">RELATED LINKS</span></span>

[<span data-ttu-id="1936a-150">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="1936a-150">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="1936a-151">제거-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="1936a-151">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="1936a-152">시작-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="1936a-152">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="1936a-153">-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="1936a-153">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="1936a-154">업데이트-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="1936a-154">Update-AzureVM</span></span>](./Update-AzureVM.md)


