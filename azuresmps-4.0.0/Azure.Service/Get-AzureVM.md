---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BBA0D5D3-29A5-4E00-9075-702E2F81CA52
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcff7873042d9f7a07eee26f93312c8690e16416
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046547"
---
# <span data-ttu-id="cb434-101">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="cb434-101">Get-AzureVM</span></span>

## <span data-ttu-id="cb434-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb434-102">SYNOPSIS</span></span>
<span data-ttu-id="cb434-103">하나 이상의 Azure 가상 컴퓨터에서 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb434-103">Retrieves information from one or more Azure virtual machines.</span></span>

## <span data-ttu-id="cb434-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cb434-104">SYNTAX</span></span>

### <span data-ttu-id="cb434-105">ListAllVMs (기본값)</span><span class="sxs-lookup"><span data-stu-id="cb434-105">ListAllVMs (Default)</span></span>
```
Get-AzureVM [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb434-106">GetVMByServiceAndVMName</span><span class="sxs-lookup"><span data-stu-id="cb434-106">GetVMByServiceAndVMName</span></span>
```
Get-AzureVM [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cb434-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cb434-107">DESCRIPTION</span></span>
<span data-ttu-id="cb434-108">**Get-help** Cmdlet은 Azure에서 실행 되는 가상 컴퓨터에 대 한 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb434-108">The **Get-AzureVM** cmdlet retrieves information about virtual machines running in Azure.</span></span>
<span data-ttu-id="cb434-109">특정 가상 컴퓨터에 대 한 정보를 포함 하는 개체를 반환 하거나, 현재 구독에 대해 지정 된 서비스의 모든 가상 컴퓨터에 대해 가상 컴퓨터를 지정 하지 않은 경우이 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb434-109">It returns an object with information on a specific virtual machine, or if no virtual machine is specified, for all the virtual machines in the specified service of the current subscription.</span></span>

## <span data-ttu-id="cb434-110">예제의</span><span class="sxs-lookup"><span data-stu-id="cb434-110">EXAMPLES</span></span>

### <span data-ttu-id="cb434-111">예제 1: 지정 된 가상 컴퓨터에서 정보 검색</span><span class="sxs-lookup"><span data-stu-id="cb434-111">Example 1: Retrieve information on a specified virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "VirtualMachine02"
```

<span data-ttu-id="cb434-112">이 명령은 ContosoService01 클라우드 서비스에서 실행 되는 VirtualMachine02 가상 컴퓨터에 대 한 정보가 포함 된 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb434-112">This command returns an object with information on the VirtualMachine02 virtual machine running in the ContosoService01 cloud service.</span></span>

### <span data-ttu-id="cb434-113">예제 2: 모든 가상 컴퓨터에 대 한 정보 검색</span><span class="sxs-lookup"><span data-stu-id="cb434-113">Example 2: Retrieve information on all virtual machines</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"
```

<span data-ttu-id="cb434-114">이 명령은 ContosoService01 클라우드 서비스에서 실행 되는 모든 가상 컴퓨터에 대 한 정보를 사용 하 여 목록 개체를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb434-114">This command retrieves a list object with information on all of the virtual machines running in the ContosoService01 cloud service.</span></span>

### <span data-ttu-id="cb434-115">예제 3: 가상 컴퓨터 상태 테이블 표시</span><span class="sxs-lookup"><span data-stu-id="cb434-115">Example 3: Display a table of virtual machine statuses</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"  | Format-Table AutoSize -Property "Name",@{Expression={$_.InstanceUpgradeDomain};Label="UpgDom";Align="Right"},"InstanceStatus"
```

<span data-ttu-id="cb434-116">이 명령은 ContosoService01 서비스에서 실행 되는 가상 컴퓨터, 해당 업그레이드 도메인, 각 가상 컴퓨터의 현재 상태를 보여 주는 테이블을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb434-116">This command displays a table showing the virtual machines running on the ContosoService01 service, their Upgrade Domain, and the current status of each virtual machine.</span></span>

## <span data-ttu-id="cb434-117">변수</span><span class="sxs-lookup"><span data-stu-id="cb434-117">PARAMETERS</span></span>

### <span data-ttu-id="cb434-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="cb434-118">-InformationAction</span></span>
<span data-ttu-id="cb434-119">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb434-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cb434-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cb434-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cb434-121">하기로</span><span class="sxs-lookup"><span data-stu-id="cb434-121">Continue</span></span>
- <span data-ttu-id="cb434-122">숨기기</span><span class="sxs-lookup"><span data-stu-id="cb434-122">Ignore</span></span>
- <span data-ttu-id="cb434-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="cb434-123">Inquire</span></span>
- <span data-ttu-id="cb434-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cb434-124">SilentlyContinue</span></span>
- <span data-ttu-id="cb434-125">중지가</span><span class="sxs-lookup"><span data-stu-id="cb434-125">Stop</span></span>
- <span data-ttu-id="cb434-126">대기</span><span class="sxs-lookup"><span data-stu-id="cb434-126">Suspend</span></span>

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

### <span data-ttu-id="cb434-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cb434-127">-InformationVariable</span></span>
<span data-ttu-id="cb434-128">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb434-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cb434-129">-이름</span><span class="sxs-lookup"><span data-stu-id="cb434-129">-Name</span></span>
<span data-ttu-id="cb434-130">정보를 검색할 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb434-130">Specifies the name of the virtual machine for which to retrieve information.</span></span>
<span data-ttu-id="cb434-131">이 매개 변수를 제공 하지 않는 경우 cmdlet은 지정 된 서비스의 모든 가상 컴퓨터에 대 한 정보를 포함 하는 list 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb434-131">If this parameter is not provided, the cmdlet returns a list object with information about all the virtual machines in the specified service.</span></span>

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb434-132">-프로필</span><span class="sxs-lookup"><span data-stu-id="cb434-132">-Profile</span></span>
<span data-ttu-id="cb434-133">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb434-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cb434-134">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="cb434-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cb434-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cb434-135">-ServiceName</span></span>
<span data-ttu-id="cb434-136">가상 컴퓨터 정보를 반환할 클라우드 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb434-136">Specifies the name of the cloud service for which to return virtual machine information.</span></span>

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb434-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb434-137">CommonParameters</span></span>
<span data-ttu-id="cb434-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb434-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb434-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb434-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb434-140">입력</span><span class="sxs-lookup"><span data-stu-id="cb434-140">INPUTS</span></span>

## <span data-ttu-id="cb434-141">출력</span><span class="sxs-lookup"><span data-stu-id="cb434-141">OUTPUTS</span></span>

## <span data-ttu-id="cb434-142">상속자</span><span class="sxs-lookup"><span data-stu-id="cb434-142">NOTES</span></span>

## <span data-ttu-id="cb434-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb434-143">RELATED LINKS</span></span>

[<span data-ttu-id="cb434-144">뉴욕</span><span class="sxs-lookup"><span data-stu-id="cb434-144">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="cb434-145">새로운 AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="cb434-145">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="cb434-146">제거-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="cb434-146">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="cb434-147">-Add-azurevm 다시 시작</span><span class="sxs-lookup"><span data-stu-id="cb434-147">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="cb434-148">시작-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="cb434-148">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="cb434-149">-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="cb434-149">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="cb434-150">업데이트-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="cb434-150">Update-AzureVM</span></span>](./Update-AzureVM.md)


