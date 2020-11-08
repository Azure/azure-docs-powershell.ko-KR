---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8A6B2633-EECC-416A-85F6-69C8341AA970
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82ef50dcdf5f17e044a9dc2091cbfda5cb5d1b2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045620"
---
# <span data-ttu-id="f89e2-101">Get-AzureRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="f89e2-101">Get-AzureRemoteDesktopFile</span></span>

## <span data-ttu-id="f89e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f89e2-102">SYNOPSIS</span></span>
<span data-ttu-id="f89e2-103">Azure 가상 컴퓨터의 RDP 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f89e2-103">Gets an RDP file for an Azure virtual machine.</span></span>

## <span data-ttu-id="f89e2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f89e2-104">SYNTAX</span></span>

### <span data-ttu-id="f89e2-105">다운로드 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f89e2-105">Download (Default)</span></span>
```
Get-AzureRemoteDesktopFile [-Name] <String> [-LocalPath] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f89e2-106">플러그인</span><span class="sxs-lookup"><span data-stu-id="f89e2-106">Launch</span></span>
```
Get-AzureRemoteDesktopFile [-Name] <String> [[-LocalPath] <String>] [-Launch] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="f89e2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f89e2-107">DESCRIPTION</span></span>
<span data-ttu-id="f89e2-108">**AzureRemoteDesktopFile** Cmdlet은 Azure 가상 컴퓨터용 RDP (원격 데스크톱 연결) 파일을 다운로드 하 여 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89e2-108">The **Get-AzureRemoteDesktopFile** cmdlet downloads and saves a remote desktop connection (RDP) file for an Azure virtual machine.</span></span>
<span data-ttu-id="f89e2-109">Cmdlet은 지정 된 가상 컴퓨터에 대 한 원격 데스크톱 연결을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f89e2-109">The cmdlet can launch a remote desktop connection to the specified virtual machine.</span></span>

## <span data-ttu-id="f89e2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f89e2-110">EXAMPLES</span></span>

### <span data-ttu-id="f89e2-111">예제 1: RDP 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="f89e2-111">Example 1: Get an RDP file</span></span>
```
PS C:\> Get-AzureRemoteDesktopFile -ServiceName "ContosoService" -Name "VirtualMachine07" -LocalPath "C:\temp\VirtualMachine07.rdp"
```

<span data-ttu-id="f89e2-112">이 명령은 ContosoService 이라는 서비스에서 실행 되는 VirtualMachine07 가상 컴퓨터 VirtualMachine07에 대 한 RDP 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f89e2-112">This command gets an RDP file for the VirtualMachine07 virtual machine named VirtualMachine07 that runs on the service named ContosoService.</span></span>
<span data-ttu-id="f89e2-113">명령이 해당 파일을 C:\temp\VirtualMachine07.rdp.로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89e2-113">The command stores that file as C:\temp\VirtualMachine07.rdp.</span></span>

### <span data-ttu-id="f89e2-114">예제 2: 원격 세션 시작</span><span class="sxs-lookup"><span data-stu-id="f89e2-114">Example 2: Start a remote session</span></span>
```
PS C:\> Get-AzureRemoteDesktopFile -ServiceName "ContosoService" -Name "VirtualMachine07" -Launch
```

<span data-ttu-id="f89e2-115">이 명령은 ContosoService 이라는 서비스에서 실행 되는 VirtualMachine07 가상 컴퓨터 VirtualMachine07에 대 한 RDP 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f89e2-115">This command gets an RDP file for the VirtualMachine07 virtual machine named VirtualMachine07 that runs on the service named ContosoService.</span></span>
<span data-ttu-id="f89e2-116">명령이 원격 데스크톱 세션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89e2-116">The command launches a remote desktop session.</span></span>
<span data-ttu-id="f89e2-117">이 명령은 연결이 닫혀 있을 때 RDP 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89e2-117">The command deletes the RDP file when the connection is closed.</span></span>

## <span data-ttu-id="f89e2-118">변수</span><span class="sxs-lookup"><span data-stu-id="f89e2-118">PARAMETERS</span></span>

### <span data-ttu-id="f89e2-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f89e2-119">-InformationAction</span></span>
<span data-ttu-id="f89e2-120">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89e2-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f89e2-121">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f89e2-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f89e2-122">하기로</span><span class="sxs-lookup"><span data-stu-id="f89e2-122">Continue</span></span>
- <span data-ttu-id="f89e2-123">숨기기</span><span class="sxs-lookup"><span data-stu-id="f89e2-123">Ignore</span></span>
- <span data-ttu-id="f89e2-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="f89e2-124">Inquire</span></span>
- <span data-ttu-id="f89e2-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f89e2-125">SilentlyContinue</span></span>
- <span data-ttu-id="f89e2-126">중지가</span><span class="sxs-lookup"><span data-stu-id="f89e2-126">Stop</span></span>
- <span data-ttu-id="f89e2-127">대기</span><span class="sxs-lookup"><span data-stu-id="f89e2-127">Suspend</span></span>

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

### <span data-ttu-id="f89e2-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f89e2-128">-InformationVariable</span></span>
<span data-ttu-id="f89e2-129">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89e2-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f89e2-130">-시작</span><span class="sxs-lookup"><span data-stu-id="f89e2-130">-Launch</span></span>
<span data-ttu-id="f89e2-131">이 cmdlet이 가상 컴퓨터에 대 한 원격 데스크톱 세션을 시작 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f89e2-131">Indicates that this cmdlet starts a remote desktop session to the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f89e2-132">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="f89e2-132">-LocalPath</span></span>
<span data-ttu-id="f89e2-133">로컬 컴퓨터에 있는 다운로드 된 RDP 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89e2-133">Specifies the full path of the downloaded RDP file on the local computer.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f89e2-134">-이름</span><span class="sxs-lookup"><span data-stu-id="f89e2-134">-Name</span></span>
<span data-ttu-id="f89e2-135">이 cmdlet이 RDP 파일을 다운로드 하는 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89e2-135">Specifies the virtual machine for which this cmdlet downloads an RDP file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f89e2-136">-프로필</span><span class="sxs-lookup"><span data-stu-id="f89e2-136">-Profile</span></span>
<span data-ttu-id="f89e2-137">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89e2-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f89e2-138">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f89e2-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f89e2-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f89e2-139">-ServiceName</span></span>
<span data-ttu-id="f89e2-140">가상 머신이 속한 Azure 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89e2-140">Specifies the name of the Azure service to which the virtual machine belongs.</span></span>

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

### <span data-ttu-id="f89e2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f89e2-141">CommonParameters</span></span>
<span data-ttu-id="f89e2-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89e2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f89e2-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f89e2-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f89e2-144">입력</span><span class="sxs-lookup"><span data-stu-id="f89e2-144">INPUTS</span></span>

## <span data-ttu-id="f89e2-145">출력</span><span class="sxs-lookup"><span data-stu-id="f89e2-145">OUTPUTS</span></span>

## <span data-ttu-id="f89e2-146">상속자</span><span class="sxs-lookup"><span data-stu-id="f89e2-146">NOTES</span></span>

## <span data-ttu-id="f89e2-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f89e2-147">RELATED LINKS</span></span>

